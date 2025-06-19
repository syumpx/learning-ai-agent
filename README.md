# 🤖 Learning AI Agent Development

A comprehensive learning repository for building AI agents using **LangChain** and **LangGraph**. This collection provides hands-on tutorials, comparisons, and practical examples to help developers understand when and how to use each framework effectively.

## 🎯 Purpose

This repository is designed to teach developers:
- **When to use LangChain vs LangGraph** for different AI workflows
- **Practical implementation patterns** for AI agents
- **Real-world scenarios** and use cases
- **Best practices** and common pitfalls
- **Progressive skill building** from basic concepts to advanced patterns

## 📚 Repository Structure

This repository is organized into weekly modules, each focusing on specific aspects of AI agent development:

| 📁 Folder | 🎯 Focus | 📋 Description | 🔗 Key Topics |
|-----------|----------|----------------|---------------|
| [`week5-motivation/`](./week5-motivation/) | **Why LangChain vs LangGraph?** | Foundational comparisons to understand when to use each framework | • Loop handling<br>• State management<br>• Framework limitations<br>• Decision criteria |

### 📖 Current Content Details

#### 🗂️ [`week5-motivation/`](./week5-motivation/)
**Objective**: Build foundational understanding of framework selection

| 📓 Notebook | 🎯 Learning Goal | ⏱️ Duration |
|-------------|------------------|-------------|
| `langchain-vs-langgraph-loop.ipynb` | Understand how each framework handles iterative workflows and loops | 30-45 min |
| `llm-call-vs-langchain.ipynb` | Compare direct LLM calls vs LangChain abstractions | 20-30 min |
| `langchain-vs-langgraph-state.ipynb` | Learn state management differences between frameworks | 25-35 min |

## 🚀 Getting Started

### Prerequisites

- **Python 3.11** 
- **Basic knowledge** of Python programming
- **Familiarity** with AI/ML concepts (helpful but not required)

### 📦 Installation & Setup

#### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/learning-ai-agent.git
cd learning-ai-agent
```

#### 2. Set Up Python Environment
```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On macOS/Linux:
source venv/bin/activate
# On Windows:
venv\Scripts\activate
```

#### 3. Install Dependencies

**Option A: Using requirements.txt (Recommended)**
```bash
# Install all dependencies at once
pip install -r requirements.txt
```

**Option B: Manual installation**
```bash
# Install Jupyter and required packages
pip install jupyter notebook

# Install all required packages for the notebooks
pip install langchain langgraph langchain-openai langchain-community langchain-core
pip install tavily-python langchain-tavily
pip install wikipedia faiss-cpu scikit-learn
pip install python-dotenv  # For .env file support
```

#### 4. Set Up API Keys

**🔑 How to get API keys:**
- **OpenAI**: Sign up at [platform.openai.com](https://platform.openai.com/)
- **Tavily**: Register at [tavily.com](https://tavily.com/) for web search functionality

**Method 1: Using .env file (Recommended)**
```bash
# Create a .env file in the repository root
touch .env

# Add your API keys to the .env file:
echo "OPENAI_API_KEY=your-openai-api-key-here" >> .env
echo "TAVILY_API_KEY=your-tavily-api-key-here" >> .env
```

**Method 2: Using environment variables**
```bash
# Set environment variables (temporary for current session)
export OPENAI_API_KEY="your-openai-api-key"
export TAVILY_API_KEY="your-tavily-api-key"

# Or add to your shell profile for persistence (.bashrc, .zshrc, etc.)
echo 'export OPENAI_API_KEY="your-openai-api-key"' >> ~/.zshrc
echo 'export TAVILY_API_KEY="your-tavily-api-key"' >> ~/.zshrc
```

**Example .env file contents:**
```bash
# Copy this template and replace with your actual keys
OPENAI_API_KEY=sk-your-openai-key-here
TAVILY_API_KEY=tvly-your-tavily-key-here
```

**⚠️ Important**: Never commit your `.env` file to git! The repository already includes `.env` in `.gitignore`.

**💡 Quick Setup Script**
```bash
# Optional: Create a setup script for convenience
cat > setup_env.sh << 'EOF'
#!/bin/bash
echo "Setting up learning-ai-agent environment..."
pip install jupyter notebook python-dotenv
pip install langchain langgraph langchain-openai langchain-community langchain-core
pip install tavily-python langchain-tavily wikipedia faiss-cpu scikit-learn
echo "Dependencies installed! Now create your .env file with API keys."
EOF

chmod +x setup_env.sh
./setup_env.sh
```

#### 5. Launch Jupyter Notebook
```bash
# Start Jupyter in the repository directory
jupyter notebook

# Or use Jupyter Lab (modern interface):
pip install jupyterlab
jupyter lab
```

### 🎓 Learning Path

**Recommended sequence for beginners:**

1. **Start with motivation** → [`week5-motivation/`](./week5-motivation/)
   - Begin with `llm-call-vs-langchain.ipynb` (basics)
   - Progress to `langchain-vs-langgraph-state.ipynb` (state concepts)
   - Finish with `langchain-vs-langgraph-loop.ipynb` (advanced patterns)

2. **Follow the weekly progression** as new content is added

### 💡 How to Use Each Notebook

1. **Open** the notebook in Jupyter
2. **Read** the introduction and learning objectives
3. **If using .env file**: Run this code in the first cell to load your API keys:
   ```python
   from dotenv import load_dotenv
   load_dotenv()  # This loads variables from .env file
   ```
4. **Run cells sequentially** (Shift + Enter)
5. **Experiment** with the provided examples
6. **Modify** parameters to see different behaviors
7. **Complete** any exercises or challenges

### 🔧 Troubleshooting

#### Common Issues:

**🚫 API Key Errors**
```bash
# Check if environment variables are set:
echo $OPENAI_API_KEY
echo $TAVILY_API_KEY

# If using .env file, make sure it's in the right location:
ls -la .env  # Should be in repository root
cat .env     # Check content (hide from others!)
```

**🚫 Import Errors**
```bash
# Reinstall all packages:
pip install --upgrade langchain langgraph langchain-openai langchain-community langchain-core
pip install --upgrade tavily-python langchain-tavily wikipedia faiss-cpu scikit-learn python-dotenv
```

**🚫 FAISS Installation Issues (macOS)**
```bash
# If faiss-cpu fails to install:
pip install faiss-cpu --no-cache-dir
# Or try:
conda install -c conda-forge faiss-cpu
```

**🚫 Jupyter Not Starting**
```bash
# Try alternative start method:
python -m jupyter notebook

# Or check if port is in use:
jupyter notebook --port=8889
```

**🚫 Deprecation Warnings**
- The notebooks may show deprecation warnings for some LangChain methods
- These are normal and won't affect functionality
- The code will continue to work while LangChain updates their APIs

## 🛣️ Roadmap

**Coming Soon:**
- 📅 **Week 1-4**: Foundation modules (planning)
- 📅 **Week 6-8**: Advanced agent patterns
- 📅 **Week 9-10**: Production deployment strategies
- 📅 **Week 11-12**: Real-world case studies

## 🤝 Contributing

This is a learning resource! Contributions welcome:

- 🐛 **Bug reports** and fixes
- 💡 **Improvement suggestions**
- 📚 **Additional examples**
- 🌍 **Translations**

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **LangChain Community** for the excellent framework
- **LangGraph Team** for innovative state management
- **Open Source Contributors** who make learning accessible

---

**📧 Questions?** Open an issue or start a discussion!

**⭐ Found this helpful?** Please star the repository to help others discover it! 
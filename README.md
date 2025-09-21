# Meesho-Dice

## Project Structure

The project is organized as follows:
```bash
groq-chatbot/
│
├── app.py              # Main Streamlit application file
├── requirements.txt    # List of Python dependencies
└── # Groq AI Chatbot 🤖

A modern, interactive chatbot application built with Streamlit and powered by Groq's lightning-fast language models. This chatbot features multiple AI personalities, conversational memory, and an intuitive web interface.

## ✨ Features

- **Multiple AI Models**: Choose between Gemma2-9B-IT and Mixtral-8x7B-32768 models
- **Personality Modes**: Select from three distinct AI personalities:
  - **Default**: Friendly and helpful assistant
  - **Expert**: Knowledgeable and authoritative with technical depth
  - **Creative**: Imaginative and inventive with unique approaches
- **Conversational Memory**: Adjustable memory length (1-10 messages) to maintain context
- **Session Statistics**: Track message count and session duration
- **Clean Interface**: Modern Streamlit UI with emojis and intuitive design
- **Chat Management**: Clear individual conversations or start fresh

## 🚀 Getting Started

### Prerequisites

- Python 3.7 or higher
- Groq API key (get one from [Groq Console](https://console.groq.com/))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/arya-io/groq-chatbot.git
   cd groq-chatbot
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up your Groq API key**
   
   Create a `.streamlit/secrets.toml` file in your project directory:
   ```toml
   groq_api_key = "your_groq_api_key_here"
   ```
   
   Or set it as an environment variable:
   ```bash
   export GROQ_API_KEY="your_groq_api_key_here"
   ```

# Steps to execute
1. mkdir -p /Users/dishant/Downloads/Code/harish/groq-chatbot/.streamlit
2. nano /Users/dishant/Downloads/Code/harish/groq-chatbot/.streamlit/secrets.toml
3. streamlit run app.py

# Sample toml file :
  # .streamlit/secrets.toml
  groq_api_key = "api key"


4. **Run the application**
   ```bash
   streamlit run app.py
   ```

5. **Open your browser**
   The app will automatically open at `http://localhost:8501`

## 🎯 Usage

### Basic Chat
1. Select your preferred AI model from the sidebar
2. Choose an AI personality that suits your needs
3. Type your message in the text area
4. Click "Send Message 🚀" to get a response

### Advanced Features
- **Adjust Memory**: Use the slider to control how many previous messages the AI remembers
- **Switch Personalities**: Change the AI's behavior style mid-conversation
- **New Conversation**: Click "Start New Conversation 🆕" to clear memory while keeping chat history
- **Clear All**: Use "Clear All Chats and Start Fresh 🗑️" to reset everything

### AI Personalities

#### Default Mode 🤝
Perfect for general conversations, questions, and everyday assistance. The AI is friendly, approachable, and provides clear, concise responses.

#### Expert Mode 🎓
Ideal for technical discussions, research questions, or when you need authoritative information. The AI provides in-depth, precise explanations with examples.

#### Creative Mode 🎨
Great for brainstorming, creative writing, or when you need innovative solutions. The AI uses metaphors, vivid descriptions, and unconventional approaches.

## 🛠️ Configuration

The application can be customized through the sidebar:

- **Model Selection**: Choose between available Groq models
- **Memory Length**: Adjust conversation context (1-10 messages)
- **Personality**: Switch between Default, Expert, and Creative modes

## 📊 Session Statistics

The sidebar displays real-time statistics:
- Total messages sent in the current session
- Session duration
- Current model and settings

## 🔧 Technical Details

### Built With
- **Streamlit**: Web application framework
- **LangChain**: LLM integration and conversation management
- **Groq**: High-performance language model API
- **Python**: Core programming language

### Architecture
- **Frontend**: Streamlit web interface
- **Backend**: LangChain conversation chains
- **Memory**: ConversationBufferWindowMemory for context retention
- **API**: Groq cloud API for model inference

### Key Components
- `initialize_session_state()`: Manages application state
- `get_custom_prompt()`: Handles personality-based prompts
- `main()`: Core application logic and UI

## 🚨 Troubleshooting

### Common Issues

**API Key Error**
```
Error: Invalid API key
```
- Ensure your Groq API key is correctly set in `secrets.toml`
- Verify the key is active and has sufficient credits

**Import Errors**
```
ModuleNotFoundError: No module named 'streamlit'
```
- Run `pip install -r requirements.txt` to install dependencies
- Consider using a virtual environment

**Port Already in Use**
```
Port 8501 is already in use
```
- Use a different port: `streamlit run app.py --server.port 8502`
- Or stop the existing Streamlit process

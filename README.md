# ViceAI

ViceAI is an advanced AI-powered assistant built on OpenAI's GPT-4. It provides an interactive chat interface, task-specific logic, and custom module integration to handle various AI-driven functionalities.

## Features

- **AI Chat Assistant**: Engage in real-time conversations with ViceAI.
- **Custom Logic**: Perform specific tasks like summarizing text or sentiment analysis.
- **Module Integration**: Extend ViceAI's functionality by integrating external Python modules.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/ViceByVirtuals/vice.git
   ```

2. Navigate to the project directory:
   ```bash
   cd vice
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Set your OpenAI API key as an environment variable:
   ```bash
   export OPENAI_API_KEY="your-openai-api-key"
   ```

2. Run the application:
   ```bash
   python vice.py
   ```

## Example Scenarios

- **Start a Chat Session**:
  ```
Welcome to Vice! Type 'exit' to end the chat.
You: What is the weather like today?
Vice: I'm not connected to a weather API, but I can answer general questions!
```

- **Summarize Text**:
  ```python
  text_to_summarize = "Vice is a powerful AI assistant that can handle multiple tasks."
  print(vice.custom_logic(task_type="summarize", text=text_to_summarize))
  ```

- **Sentiment Analysis**:
  ```python
  text_to_analyze = "I love working with AI technologies!"
  print(vice.custom_logic(task_type="analyze_sentiment", text=text_to_analyze))
  ```

## Custom Module Integration

To integrate a custom module, create a Python module with a `run()` method. Example:

```python
# mymodule.py
def run(data):
    return f"Processing data: {data}"
```

Integrate it as follows:
```python
result = vice.integrate_custom_functionality("mymodule", data="Sample Data")
print(result)
```

## Contributing

We welcome contributions! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.

## Contact

For support or collaboration, please contact the development team at **support@viceagent.com**.


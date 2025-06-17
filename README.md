# 🛫 Travel Agency Assistant - Day 5 Project

A comprehensive AI-powered travel assistant built with OpenAI's GPT models, featuring chat capabilities, image generation, and audio processing. This project demonstrates advanced function calling, multimodal AI interactions, and web interface development using Gradio.

## ✨ Features

- 💬 **Intelligent Chat Interface**: Natural language conversation with travel expertise
- 🖼️ **Destination Image Generation**: AI-generated vibrant pop-art style destination images using DALL-E
- 🔊 **Text-to-Speech**: Audio responses with OpenAI's TTS models
- 🎵 **Audio Processing**: Advanced audio handling with multiple format support
- 🌍 **Travel Expertise**: Specialized knowledge about destinations, travel tips, and recommendations
- 🖥️ **Modern Web Interface**: Interactive Gradio-based UI with real-time chat and media display

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- OpenAI API key with access to:
  - GPT models (gpt-4o-mini or similar)
  - DALL-E for image generation
  - TTS models for audio synthesis
- FFmpeg (for audio processing)

### Installation

1. **Navigate to the project directory**:
   ```bash
   cd llm_engineering/travel_agency
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**:
   Create a `.env` file in the project directory:
   ```env
   OPENAI_API_KEY=sk-proj-your-openai-api-key-here
   ```

4. **Run the Jupyter notebook**:
   ```bash
   jupyter notebook travel_agency.ipynb
   ```
   
   Or use JupyterLab:
   ```bash
   jupyter lab travel_agency.ipynb
   ```

## 📚 Usage

### Running the Notebook

1. Open `travel_agency.ipynb` in Jupyter
2. Run all cells to initialize the assistant
3. The final cell will launch a Gradio interface
4. Interact with the travel assistant through the web interface

### Example Interactions

- **Destination Inquiry**: "I want to travel to Paris, what should I know?"
- **Image Generation**: Ask about any destination and receive beautiful AI-generated artwork
- **Travel Advice**: "What are the best destinations for summer vacation?"
- **Audio Responses**: Enable TTS for spoken responses to your queries

### Key Components

#### Chat Functionality
The assistant provides expert travel advice using OpenAI's chat completion API with specialized system prompts for travel expertise.

#### Image Generation
- Automatically generates destination images in vibrant pop-art style
- Uses DALL-E to create unique visual representations of travel destinations
- Images are displayed directly in the chat interface

#### Audio Processing
- Text-to-speech conversion for assistant responses
- Multiple audio format support (MP3, WAV, etc.)
- Cross-platform audio playback capabilities

## 🏗️ Technical Architecture

### Core Components

- **OpenAI Integration**: GPT models for chat, DALL-E for images, TTS for audio
- **Gradio Interface**: Modern web UI with chat, image, and audio components
- **Audio Processing**: Pydub and system audio tools for multimedia handling
- **Image Processing**: PIL/Pillow for image manipulation and display
- **Environment Management**: Secure API key handling with python-dotenv

### Function Structure

```python
# Main chat function with image generation
def chat(message, history):
    # Processes user messages
    # Generates AI responses
    # Creates destination images when relevant
    # Returns updated chat history and images

# Image generation function
def artist(city):
    # Uses DALL-E to generate destination artwork
    # Returns PIL Image objects for display

# Audio processing functions
# Handle TTS conversion and audio playback
```

## 🔧 Configuration

### Environment Variables

```env
# Required
OPENAI_API_KEY=sk-proj-your-openai-api-key-here

# Optional OpenAI model configurations
OPENAI_MODEL=gpt-4o-mini
TTS_MODEL=tts-1
TTS_VOICE=alloy
IMAGE_MODEL=dall-e-3
```

### Gradio Interface Options

The notebook includes both simple and advanced Gradio interfaces:
- **Simple Interface**: Basic chat with automatic features
- **Advanced Interface**: Separate panels for chat, images, and audio controls

## 📋 Project Structure

```
llm_engineering/travel_agency/
├── travel_agency.ipynb  # Main notebook with complete implementation
├── README.md           # This documentation
├── requirements.txt    # Python dependencies
└── .env               # Environment variables (create this)
```

## 🐛 Troubleshooting

### Common Issues

1. **OpenAI API Errors**:
   - Verify your API key is valid and has sufficient credits
   - Ensure you have access to GPT, DALL-E, and TTS models
   - Check rate limits if experiencing frequent errors

2. **Audio Issues**:
   - Install FFmpeg for audio processing
   - On Windows, ensure FFmpeg is in your system PATH
   - Try different audio formats if playback fails

3. **Image Generation Failures**:
   - Verify DALL-E API access
   - Check content policy compliance for image prompts
   - Monitor usage quotas for image generation

4. **Gradio Interface Issues**:
   - Ensure port 7860 is available (or modify in notebook)
   - Check firewall settings for local web server
   - Try refreshing the browser if interface doesn't load

### Debug Tips

- Run cells individually to isolate issues
- Check the notebook output for detailed error messages
- Verify all imports are successful before running main functions
- Use print statements to debug API responses

## 🎓 Learning Objectives

This project demonstrates:

- **Advanced OpenAI API Usage**: Multi-model integration (GPT + DALL-E + TTS)
- **Function Calling**: Structured AI interactions with custom tools
- **Multimodal AI**: Combining text, image, and audio in one application
- **Web Interface Development**: Creating interactive UIs with Gradio
- **Audio Processing**: Handling multimedia content in Python applications
- **API Integration**: Professional patterns for external service integration

## 📖 Additional Resources

- [OpenAI API Documentation](https://platform.openai.com/docs)
- [Gradio Documentation](https://gradio.app/docs)
- [DALL-E API Guide](https://platform.openai.com/docs/guides/images)
- [OpenAI TTS Documentation](https://platform.openai.com/docs/guides/text-to-speech)

## 🤝 Contributing

This is an educational project from the LLM Engineering course. Feel free to:
- Experiment with different prompts and models
- Add new travel-related functions
- Enhance the UI with additional Gradio components
- Implement additional audio/image processing features

## 📝 License

Educational project - feel free to use and modify for learning purposes.

---

*Part of the LLM Engineering course - Day 5 Travel Agency Assistant project* 
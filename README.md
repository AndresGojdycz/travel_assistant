# 🛫 Travel Agency Assistant - Day 5 Project

A comprehensive AI-powered travel assistant built with **OpenAI's Agents Framework**, featuring advanced function calling, multimodal AI interactions, and immersive audio experiences. This project demonstrates cutting-edge agent-based architecture, intelligent tool usage, and professional-grade audio processing capabilities using Gradio's modern web interface.

## ✨ Core Features

### 🤖 **AI Agents Framework**
- **Function Calling Agents**: Advanced OpenAI agents with structured tool usage and decision-making
- **Multi-Tool Integration**: Seamless coordination between chat, image generation, and audio processing tools
- **Intelligent Context Management**: Persistent conversation memory with context-aware responses
- **Autonomous Task Execution**: Self-directed agent behavior for travel planning and recommendations

### 🔊 **Advanced Audio System**
- **OpenAI TTS Integration**: High-quality text-to-speech with multiple voice options (`alloy`, `echo`, `fable`, `onyx`, `nova`, `shimmer`)
- **Real-time Audio Processing**: Live audio generation and playback with cross-platform compatibility
- **Audio Format Support**: MP3, WAV, and multiple audio formats with automatic conversion
- **Interactive Audio Controls**: Play/pause, volume control, and download functionality
- **Audio Streaming**: Efficient audio streaming and buffering for seamless user experience

### 🎨 **Multimodal Capabilities**
- 💬 **Intelligent Chat Interface**: Natural language conversation with specialized travel expertise
- 🖼️ **AI-Generated Destination Art**: Vibrant pop-art style images using DALL-E 3
- 🌍 **Travel Intelligence**: Comprehensive destination knowledge and personalized recommendations
- 🖥️ **Modern Web Interface**: Interactive Gradio-based UI with real-time multimedia display

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- OpenAI API key with access to:
  - **GPT models** (gpt-4o-mini or gpt-4) for agents framework
  - **DALL-E 3** for image generation
  - **TTS models** (tts-1, tts-1-hd) for audio synthesis
- **FFmpeg** (required for audio processing and format conversion)

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

## 📚 Usage Guide

### Agent Interactions

The travel assistant uses OpenAI's function calling framework to provide intelligent, context-aware responses:

- **Destination Planning**: "I want a 7-day itinerary for Japan in spring"
- **Visual Discovery**: Ask about any destination to receive AI-generated artwork
- **Audio Experiences**: Enable TTS for immersive spoken responses
- **Interactive Planning**: Multi-turn conversations with persistent context

### Audio Features

#### Text-to-Speech Configuration
- **Voice Selection**: Choose from 6 premium OpenAI voices
- **Audio Quality**: Support for both standard (`tts-1`) and HD (`tts-1-hd`) models
- **Real-time Processing**: Instant audio generation and playback
- **Download Options**: Save audio responses for offline use

#### Audio Processing Pipeline
```python
# Audio generation and processing workflow
OpenAI TTS API → Audio Buffer → Pydub Processing → Format Conversion → Gradio Playback
```

## 🏗️ Technical Architecture

### Agents Framework Implementation

#### Core Agent Components
- **System Prompts**: Specialized travel expertise and personality configuration
- **Function Definitions**: Structured tool definitions for image generation and audio processing
- **Context Management**: Conversation history and state persistence
- **Tool Orchestration**: Intelligent decision-making for tool usage

#### Function Calling Structure
```python
# Agent function calling pipeline
User Input → Agent Analysis → Tool Selection → Function Execution → Response Generation
```

### Audio Processing Architecture

#### Audio Pipeline Components
- **TTS Engine**: OpenAI's advanced text-to-speech models
- **Audio Processing**: Pydub for format conversion and manipulation
- **Streaming**: Efficient audio buffering and delivery
- **Cross-platform Playback**: Support for Windows, macOS, and Linux

#### Audio Processing Flow
```python
def audio_pipeline(text, voice="alloy", model="tts-1"):
    # OpenAI TTS generation
    response = openai.audio.speech.create(
        model=model,
        voice=voice,
        input=text
    )
    
    # Audio processing with Pydub
    audio_segment = AudioSegment.from_file(BytesIO(response.content))
    
    # Format conversion and optimization
    return optimized_audio_for_web_playback()
```

### Integration Architecture

- **OpenAI Integration**: Multi-model coordination (GPT + DALL-E + TTS)
- **Gradio Interface**: Advanced web UI with multimedia components
- **Audio Processing**: Professional-grade audio handling with Pydub
- **Image Processing**: PIL/Pillow for image manipulation and display
- **Environment Management**: Secure API key handling with python-dotenv

## 🔧 Advanced Configuration

### Agent Configuration

```env
# Core API Configuration
OPENAI_API_KEY=sk-proj-your-openai-api-key-here

# Agent Model Settings
OPENAI_MODEL=gpt-4o-mini
AGENT_TEMPERATURE=0.7
MAX_TOKENS=2048

# Audio Configuration
TTS_MODEL=tts-1-hd
TTS_VOICE=alloy
AUDIO_FORMAT=mp3
AUDIO_QUALITY=high

# Image Generation
IMAGE_MODEL=dall-e-3
IMAGE_SIZE=1024x1024
IMAGE_STYLE=vivid
```

### Audio System Configuration

#### Voice Options
- **alloy**: Balanced and versatile
- **echo**: Clear and professional  
- **fable**: Warm and engaging
- **onyx**: Deep and authoritative
- **nova**: Youthful and energetic
- **shimmer**: Soft and calming

#### Audio Quality Settings
- **Standard TTS (`tts-1`)**: Fast generation, good quality
- **HD TTS (`tts-1-hd`)**: Higher quality, slightly slower generation

## 🎓 Learning Objectives

This project demonstrates advanced concepts in:

### AI Agents Development
- **Function Calling Frameworks**: Implementing structured AI agents with tool usage
- **Multi-Agent Coordination**: Managing multiple AI capabilities in a single interface
- **Context Management**: Maintaining conversation state and memory
- **Tool Integration**: Seamlessly connecting different AI services and APIs

### Audio Processing & TTS
- **Professional Audio Pipeline**: End-to-end audio generation and processing
- **Cross-platform Audio**: Handling audio across different operating systems
- **Real-time Processing**: Streaming audio generation and playback
- **Format Optimization**: Audio compression and format conversion for web delivery

### System Integration
- **Multimodal AI**: Combining text, image, and audio in unified applications
- **Web Interface Development**: Creating interactive UIs with Gradio
- **API Architecture**: Professional patterns for external service integration
- **Error Handling**: Robust error management for production-ready applications

## 🐛 Troubleshooting

### Agent Framework Issues

1. **Function Calling Errors**:
   - Verify OpenAI API access to function calling models
   - Check function definition schemas for correctness
   - Monitor token usage and context length limits

2. **Context Management**:
   - Implement conversation history pruning for long sessions
   - Manage system message consistency
   - Handle context overflow gracefully

### Audio System Issues

1. **TTS Generation Problems**:
   - Verify OpenAI TTS API access and quotas
   - Check voice model availability in your region
   - Monitor audio generation rate limits

2. **Audio Playback Issues**:
   - Install FFmpeg and ensure it's in system PATH
   - Check browser audio permissions and settings
   - Try different audio formats if playback fails
   - Verify Pydub installation and dependencies

3. **Cross-platform Audio**:
   - **Windows**: Ensure FFmpeg is properly installed
   - **macOS**: Install FFmpeg via Homebrew: `brew install ffmpeg`
   - **Linux**: Install via package manager: `sudo apt install ffmpeg`

### Performance Optimization

- **Audio Caching**: Implement audio response caching for repeated queries
- **Async Processing**: Use asynchronous audio generation for better UX
- **Batch Processing**: Process multiple audio requests efficiently
- **Memory Management**: Optimize audio buffer handling for large files

## 📖 Additional Resources

### OpenAI Documentation
- [Function Calling Guide](https://platform.openai.com/docs/guides/function-calling)
- [TTS API Documentation](https://platform.openai.com/docs/guides/text-to-speech)
- [DALL-E API Guide](https://platform.openai.com/docs/guides/images)
- [Chat Completions API](https://platform.openai.com/docs/guides/text-generation)

### Audio Processing Resources
- [Pydub Documentation](https://pydub.com/)
- [FFmpeg Documentation](https://ffmpeg.org/documentation.html)
- [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)

### Framework Documentation
- [Gradio Documentation](https://gradio.app/docs)
- [Jupyter Notebook Guide](https://jupyter-notebook.readthedocs.io/)

## 🤝 Contributing

This is an educational project from the LLM Engineering course. Contribute by:
- **Enhancing Agent Capabilities**: Add new function calling tools
- **Improving Audio Features**: Implement advanced audio processing
- **UI/UX Enhancements**: Expand Gradio interface capabilities
- **Performance Optimization**: Optimize audio streaming and processing
- **Multi-language Support**: Add TTS support for multiple languages

## 📝 License

Educational project - feel free to use and modify for learning purposes.

---

*Part of the LLM Engineering course - Day 5 Travel Agency Assistant project featuring advanced AI agents and professional audio processing* 
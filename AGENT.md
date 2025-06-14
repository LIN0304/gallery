# Google AI Edge Gallery Agent

## Overview

Google AI Edge Gallery is an experimental Android application that demonstrates the power of on-device generative AI models. The application enables users to run cutting-edge AI models directly on their devices without requiring an internet connection after initial model download.

## Core Capabilities

### Model Execution
- **Local Processing**: All AI computations occur on-device, ensuring privacy and offline functionality
- **Model Flexibility**: Support for multiple models from Hugging Face with seamless switching
- **Custom Model Support**: Ability to test local LiteRT `.task` models

### Feature Set
1. **Ask Image**: Upload images and ask questions for descriptions, problem-solving, or object identification
2. **Prompt Lab**: Single-turn LLM use cases including summarization, rewriting, and code generation
3. **AI Chat**: Multi-turn conversational interactions
4. **Performance Metrics**: Real-time benchmarks including TTFT, decode speed, and latency

## Technical Architecture

### Technology Stack
- **Google AI Edge**: Core APIs and tools for on-device machine learning
- **LiteRT**: Lightweight runtime optimized for model execution
- **LLM Inference API**: Powers on-device Large Language Models
- **Hugging Face Integration**: Model discovery and download capabilities

### Supported Models

Based on model_allowlist.json, the application supports:

1. **Gemma-3n-E2B-it-int4**
   - Size: 3.14GB
   - Peak Memory: 5.91GB
   - Supports: Text, vision input (4096 context length)
   - Task Types: llm_chat, llm_prompt_lab, llm_ask_image

2. **Gemma-3n-E4B-it-int4**
   - Size: 4.41GB
   - Peak Memory: 6.98GB
   - Supports: Text, vision input (4096 context length)
   - Task Types: llm_chat, llm_prompt_lab, llm_ask_image

3. **Gemma3-1B-IT q4**
   - Size: 555MB
   - Peak Memory: 2.15GB
   - Supports: Text input
   - Task Types: llm_chat, llm_prompt_lab

4. **Qwen2.5-1.5B-Instruct q8**
   - Size: 1.63GB
   - Peak Memory: 2.68GB
   - Supports: Text input
   - Task Types: llm_chat, llm_prompt_lab

## Repository Structure

### Issue Templates
The repository includes three standardized issue templates:
- Bug reports for tracking and resolving issues
- Feature requests for proposing enhancements
- Support requests for user assistance

### Build Configuration
- Android APK builds via GitHub Actions workflow
- Automated builds triggered on main branch changes to Android directory

## Current Status

### Development Phase
- **Stage**: Experimental Alpha release
- **Platform Availability**: 
  - Android: Available now
  - iOS: Coming soon
- **Contribution Status**: Not currently accepting code contributions

### Installation
- Primary method: Download latest APK from GitHub releases
- Additional installation guidance available in project wiki

## Key Considerations

### Performance Requirements
- Device must support the memory requirements of selected models
- GPU acceleration available for supported models
- CPU fallback for broader compatibility

### Privacy and Security
- All processing occurs on-device
- No data transmitted to external servers during inference
- Internet required only for initial model download

## Future Roadmap

### Planned Enhancements
- iOS platform support
- Expanded model library
- Enhanced performance optimization
- Community contribution framework (pending announcement)

## Developer Resources

### Documentation Links
- [Project Wiki](https://github.com/google-ai-edge/gallery/wiki)
- [LLM Inference Guide for Android](https://ai.google.dev/edge/mediapipe/solutions/genai/llm_inference/android)
- [Google AI Edge Documentation](https://ai.google.dev/edge)
- [Hugging Face LiteRT Community](https://huggingface.co/litert-community)

### Technical Integration Points
- MediaPipe LLM Inference API
- LiteRT model format (.task files)
- Hugging Face model repository integration

## Usage Guidelines

### Model Selection
1. Consider device capabilities versus model requirements
2. Balance performance needs with accuracy requirements
3. Test custom models using the "Bring Your Own Model" feature

### Optimization Strategies
- Use GPU acceleration when available
- Select appropriate quantization levels
- Monitor performance metrics for bottleneck identification

## Support and Feedback

### Reporting Issues
- Use appropriate issue template (bug, feature, support)
- Provide detailed environment information
- Include screenshots or videos when applicable

### Community Engagement
- Monitor GitHub releases for updates
- Participate in issue discussions
- Await contribution guidelines announcement

## License
Licensed under Apache License 2.0, promoting open-source collaboration while maintaining appropriate usage guidelines.

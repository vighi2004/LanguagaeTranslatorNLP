
# Language Translator Web App with Audio & Text-to-Speech

A modern, full-stack Natural Language Processing (NLP) web application built using Flask and powered by advanced translation and speech synthesis engines. This project features a beautiful glassmorphism UI, real-time machine translation, text-to-speech capabilities, and public sharing functionalities via ngrok.

✨ Features

• ⚡ Multi-Language Translation: Seamlessly translate between 11 major global and regional Indian languages.
• 🔊 Text-to-Speech (TTS): Synthesize translated text into lifelike spoken audio with a click of a button.
• 🎨 Glassmorphism UI: A sleek, fully responsive frontend design built with custom CSS blur backdrops.
• 📋 Clipboard Integration: One-click copy function with dynamic UI state feedback.
• 🚀 Cloud-Ready Deployment: Native compatibility with Google Colab and easy local execution.
• 🌐 Public Tunneling: Securely expose your local server to the global internet using pyngrok.

🧠 NLP & Machine Learning Architecture

This application acts as an accessible pipeline bridging user-facing design with state-of-the-art backend NLP models:

1. Machine Translation Ecosystem (NMT)

Instead of legacy token-replacement matrices, the application harnesses Neural Machine Translation (NMT) through the deep-translator framework.
• How it works: It paths requests into massive, deep sequence-to-sequence (Seq2Seq) neural networks.
• Contextual Awareness: The underlying model utilizes modern attention mechanisms to read whole sentences globally, ensuring translated text preserves contextual syntax, structural idioms, and regional grammar mappings rather than literal word-by-word swaps.

2. Audio Synthesis (TTS Pipeline)

The system leverages Google's gTTS (Google Text-to-Speech) engine to read localized string sequences.
• Waveform Synthesis: Text token outputs are converted into high-fidelity acoustic parameters.
• Audio Streaming: Rather than cluttering server hardware with hard-drive intensive .mp3 caching, the application captures raw sound data as an in-memory binary stream (io.BytesIO). It then directly pushes the buffer payload to the frontend client pipeline over standard MIME types for instantaneous playback.

🛠️ Tech Stack

• Backend: Python, Flask
• NLP Engines: Deep-Translator (Google Neural Translation API Integration), gTTS
• Frontend: HTML5, CSS3 (Modern Flexbox Grid & Glassmorphism framework), JavaScript (Async/Fetch API)
• Tunneling Service: Pyngrok

🚀 Quick Start Guide


Prerequisites

Before launching, ensure you have a free Auth Token from ngrok.
1. Sign up or log into dashboard.ngrok.com.
2. Copy your unique token from the Your Authtoken section.

Installation

If you are running the project locally, install the necessary dependencies via your terminal:
bash
pip install Flask pyngrok deep-translator gTTS
Use code with caution.
(Note: If you run this inside Google Colab, the environment will dynamically execute these installations automatically).

Configuration & Running

1. Open the project file and locate the configuration segment inside the __main__ entry hook:
python
# Insert your ngrok authentication key here
NGROK_AUTH_TOKEN = "your_actual_ngrok_token_here"
Use code with caution.
2. Execute the Python script:
bash
python app.py
Use code with caution.
3. Look at your console terminal output. The application will fetch a secure public tunnel URL:
text
 * ngrok tunnel "https://ngrok-free.app" -> "http://127.0.0.1:5000"
Use code with caution.
4. Click the generated .ngrok-free.app link to interact with your live application or share it with others!

🗺️ Supported Languages

The application comes pre-configured with core mappings across global and regional systems:
• 🇬🇧 English (en)
• 🇮🇳 Hindi (hi)
• 🇮🇳 Bengali (bn)
• 🇮🇳 Tamil (ta)
• 🇮🇳 Telugu (te)
• 🇮🇳 Marathi (mr)
• 🇮🇳 Gujarati (gu)
• 🇮🇳 Kannada (kn)
• 🇮🇳 Malayalam (ml)
• 🇮🇳 Punjabi (pa)
• 🇵🇰 Urdu (ur)

🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to fork the repository, make alterations, and submit a pull request.

# TranslaCall

TranslaCall is an open-source project aimed at creating a real-time voice translation service that enables seamless communication across different languages through a simple phone call. By leveraging advanced AI and language models, TranslaCall removes language barriers without the need for apps, internet access, or specialized devices.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Architecture](#architecture)
- [Roadmap](#roadmap)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Configuration](#configuration)
- [Usage](#usage)
  - [Local Limited Version](#local-limited-version)
  - [Cloud-Hosted Version](#cloud-hosted-version)
- [Contribution Guidelines](#contribution-guidelines)
- [Community and Support](#community-and-support)
- [License](#license)
- [Contact](#contact)

## Introduction

TranslaCall aims to break down language barriers by providing an accessible, real-time voice translation service that works over standard phone calls. This project is designed to be inclusive and user-friendly, especially for individuals without access to smartphones or the internet.

## Features

- **Universal Accessibility**: Operates over standard phone lines, requiring no internet connection or smartphone.
- **Real-Time Translation**: Provides low-latency, real-time voice translation between multiple languages.
- **Voice Replication**: Preserves the speaker's voice characteristics, tone, and emotional intonations.
- **Flexible Deployment**:
  - **Local Limited Version**: Run a basic version locally for development or personal use.
  - **Cloud-Hosted Version**: Access a fully-featured hosted service for ease of use.
- **Scalable Architecture**: Designed to handle a growing number of users efficiently.
- **Privacy and Security**: Ensures user confidentiality and complies with data protection regulations.
- **Extensible**: Modular design allows for easy integration of additional languages and features.

## Architecture

The TranslaCall system consists of several key components:

1. **Telephony Interface**: Manages incoming and outgoing phone calls using services like Twilio or alternative open-source telephony solutions (e.g., Asterisk).
2. **Speech Recognition Module**: Converts spoken language into text using ASR (Automatic Speech Recognition) engines.
3. **Translation Engine**: Translates text from one language to another using machine translation services or models.
4. **Speech Synthesis Module**: Converts translated text back into speech, replicating the original speaker's voice characteristics.
5. **Session Manager**: Handles call sessions, routing, and state management.
6. **User Interface**: Provides interaction through voice prompts and SMS messages.
7. **Payment Processing (Cloud-Hosted Version)**: Manages subscription plans, usage tracking, and payment transactions.
8. **Data Storage**: Stores configuration settings, usage logs, and user preferences securely.

![Architecture Diagram](./docs/architecture-diagram.png)

*Note: An architecture diagram illustrating system components and interactions will be added in future updates.*

## Roadmap

- **Phase 1**: Development of the core system with basic functionalities.
  - Implement telephony interface.
  - Integrate speech recognition and synthesis modules.
  - Set up translation engine using open-source tools.
- **Phase 2**: Enhancement of features and performance.
  - Improve real-time translation latency.
  - Integrate voice replication technology.
  - Add support for additional languages.
- **Phase 3**: Deployment options and scalability.
  - Provide easy deployment scripts for local setup.
  - Develop the cloud-hosted version with scalable infrastructure.
  - Implement payment processing and subscription management (for cloud version).
- **Phase 4**: Community engagement and expansion.
  - Foster a developer community for contributions.
  - Gather user feedback for continuous improvement.
  - Explore partnerships and integrations.

## Getting Started

### Prerequisites

- **Programming Languages**: Python 3.8+
- **Frameworks and Libraries**:
  - Flask or Django for web server and API endpoints.
  - Speech recognition libraries (e.g., Vosk, PocketSphinx).
  - Speech synthesis libraries (e.g., eSpeak, Festival).
  - Translation libraries or services (e.g., OpenNMT, Marian NMT).
- **Telephony Services**:
  - **For Local Version**: Optional, can use simulated calls.
  - **For Full Functionality**: Twilio account or an open-source telephony platform like Asterisk.
- **Database**:
  - SQLite for local development.
  - PostgreSQL or MongoDB for production environments.

### Installation

1. **Clone the Repository**

   <code>
   git clone https://github.com/tomchapin/translacall.git  
   cd translacall
   </code>

2. **Create a Virtual Environment**

   <code>
   python3 -m venv venv  
   source venv/bin/activate
   </code>

3. **Install Dependencies**

   <code>
   pip install -r requirements.txt
   </code>

### Configuration

1. **Set Up Environment Variables**

   Create a `.env` file in the project root directory and add the necessary configurations.

   <code>
   # General Settings  
   SECRET_KEY=your_secret_key  
   DEBUG=True

   # Telephony Settings (if using Twilio)  
   TWILIO_ACCOUNT_SID=your_twilio_account_sid  
   TWILIO_AUTH_TOKEN=your_twilio_auth_token  
   TWILIO_PHONE_NUMBER=your_twilio_phone_number

   # Speech Recognition and Synthesis Settings  
   ASR_ENGINE=vosk  
   TTS_ENGINE=espeak

   # Translation Settings  
   TRANSLATION_ENGINE=opennmt

   # Database Settings  
   DATABASE_URL=sqlite:///translacall.db
   </code>

2. **Run Database Migrations**

   <code>
   # For Django  
   python manage.py migrate

   # For Flask (if using Flask-Migrate)  
   flask db upgrade
   </code>

3. **Start the Server**

   <code>
   # For Django  
   python manage.py runserver

   # For Flask  
   flask run
   </code>

## Usage

### Local Limited Version

The local version allows you to test and develop TranslaCall on your machine.

- **Simulate Calls**: Use provided scripts to simulate incoming and outgoing calls.
- **Test Translations**: Verify translation functionalities between selected languages.
- **Extend and Customize**: Modify the code to add new features or integrate different modules.

### Cloud-Hosted Version

For full functionality without setup complexity:

1. **Sign Up**

   Visit [www.translacall.com](https://www.translacall.com) to create an account.

2. **Select a Plan**

   Choose a subscription plan or pay-per-use option that fits your needs.

3. **Start Using TranslaCall**

   Follow the instructions to begin making real-time translated calls.

## Contribution Guidelines

We welcome contributions from the community! To contribute:

1. **Fork the Repository**

   Click on the 'Fork' button at the top right corner of the repository page.

2. **Create a Feature Branch**

   <code>
   git checkout -b feature/your-feature-name
   </code>

3. **Commit Your Changes**

   <code>
   git commit -m "Add your descriptive commit message"
   </code>

4. **Push to Your Fork**

   <code>
   git push origin feature/your-feature-name
   </code>

5. **Submit a Pull Request**

   Open a pull request to the main repository with a detailed description of your changes.

### Coding Standards

- Follow PEP 8 style guidelines for Python code.
- Write clear, concise commit messages.
- Include docstrings and comments where necessary.

### Reporting Issues

- Use GitHub Issues to report bugs or suggest enhancements.
- Provide as much detail as possible, including steps to reproduce the issue.

## Community and Support

- **Discussion Forum**: Join our [GitHub Discussions](https://github.com/tomchapin/translacall/discussions) to engage with other users and developers.
- **Chat**: Connect with the community on [Discord](https://discord.gg/yourinvitelink) or [Slack](https://yourworkspace.slack.com).
- **Email Support**: For direct inquiries, email us at [translacall@phaseinteractive.com](mailto:translacall@phaseinteractive.com).

## License

This project is licensed under the [MIT License](./LICENSE).

## Contact

For questions, suggestions, or collaboration opportunities, please contact:

- **Email**: [translacall@phaseinteractive.com](mailto:translacall@phaseinteractive.com)
- **GitHub Issues**: Submit an issue on the repository.

---

**Note**: This project is in active development. Your contributions and feedback are invaluable in making TranslaCall a success.

---

## Acknowledgments

- **Open-Source Libraries**: We thank the developers of the open-source tools and libraries used in this project.
- **Community Contributors**: Special thanks to all contributors who have helped shape TranslaCall.

---

## Disclaimer

TranslaCall is provided "as is" without warranty of any kind. The use of third-party services may incur costs and are subject to their respective terms and conditions.

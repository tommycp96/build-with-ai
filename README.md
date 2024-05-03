# Build with AI

Welcome to the **Build with AI** project! This application allows users to interact with the Gemini 1.5 Pro Preview model via a user-friendly web interface, leveraging Google Cloud services. It's built using Flask for the backend and Tailwind CSS for styling.

## Overview

This project demonstrates how to integrate the latest AI technologies with a web application. The app accepts user prompts, processes them using Google Vertex AI, and displays the AI's responses in a clean, styled format.

> This project has been deployed to my Cloud Run and publicly accessible through this URL https://build-with-ai-sw52hvjzda-uc.a.run.app

## Features

- **AI-Driven Responses**: Users can input prompts and receive AI-generated responses in markdown format.
- **Responsive UI**: The application uses Tailwind CSS for a clean and responsive design.
- **Cloud-Native**: The application is hosted on Google Cloud Run, ensuring scalability and security.

## Tech Stack

- **Backend**: Flask
- **Frontend**: Tailwind CSS
- **AI Model**: Gemini 1.5 Pro Preview
- **Cloud**: Google Cloud Run and Google Vertex AI

## Getting Started

### Prerequisites

To run this project locally, you need:

1. Python 3.7+ installed.
2. A Google Cloud Platform account with the necessary permissions for Vertex AI and Cloud Run.

### Installation

1. **Clone the repository**:
   ```sh
   git clone https://github.com/tommycp96/build-with-ai.git
   ```
2. **Navigate to the project directory**:
   ```sh
   cd build-with-ai
   ```
3. **Create a virtual environment**:
   ```sh
   python3 -m venv venv
   ```
4. **Activate the virtual environment**:

   - On Windows:
     ```sh
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```sh
     source venv/bin/activate
     ```

5. **Install dependencies**:

   ```sh
   pip install -r requirements.txt
   ```

6. **Run the application locally**:
   ```sh
   flask run
   ```

### Deployment

To deploy this application on Google Cloud Run:

1. **Build and push the container**:

   ```sh
   gcloud builds submit --tag gcr.io/[PROJECT-ID]/[IMAGE-NAME]
   ```

2. **Deploy to Cloud Run**:

   ```sh
   gcloud run deploy --image gcr.io/[PROJECT-ID]/[IMAGE-NAME] --platform managed
   ```

### Configuration

Make sure to set up the necessary service accounts and permissions to use the Gemini 1.5 Pro Preview model on Google Vertex AI. The configuration details for the Vertex AI integration should be managed via environment variables or other secure methods to protect sensitive information.

## Usage

1. **Submit a Prompt**:

   - Enter a prompt into the input field and click "Submit."
   - The application will display a loading spinner while processing the input.
   - The AI response will be displayed in markdown format.

2. **Modify Input**:
   - The input field can be modified or cleared to input a new prompt.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements

- **Google Cloud** for the robust cloud platform.
- **Tailwind CSS** for the intuitive frontend framework.
- **Flask** for the lightweight web framework.

## Contact

For further inquiries or support, please contact Tommy, the developer, via the repository's contact information.

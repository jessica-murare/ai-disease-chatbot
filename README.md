# HealthBot: AI-Powered Disease Chatbot

This is the repository for HealthBot, a chatbot designed to provide information about diseases, healthcare FAQs, outbreak alerts, and vaccination schedules. This chatbot is built using the [Rasa](https://rasa.com/) framework.

## Project Structure

- `actions/`: Contains the code for custom actions.
- `data/`: Contains the NLU training data, stories, and rules.
- `knowledge_base/`: Contains the knowledge base for the chatbot in JSON format.
- `models/`: Contains the trained Rasa models.
- `config.yml`: The main configuration file for the Rasa model.
- `domain.yml`: The domain file for the chatbot, defining intents, entities, slots, responses, and actions.
- `endpoints.yml`: The endpoints configuration file for connecting to custom actions and other services.
- `requirements.txt`: The Python dependencies for this project.
- `.gitignore`: Specifies intentionally untracked files to ignore.
- `.rasa/`: Caches information between training runs.
- `.venv/`: Contains the Python virtual environment.

## Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/ai-disease-chatbot.git
    cd ai-disease-chatbot
    ```
2.  **Create a virtual environment and install dependencies:**
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows, use `.venv\Scripts\activate`
    pip install -r requirements.txt
    ```

## Usage

1.  **Train the Rasa model:**
    ```bash
    rasa train
    ```
2.  **Run the action server:**
    ```bash
    rasa run actions
    ```
3.  **Run the chatbot:**
    In a new terminal, run:
    ```bash
    rasa shell
    ```

## Knowledge Base

The chatbot uses a knowledge base to answer questions about:

-   **Healthcare FAQs:** `knowledge_base/healthcare_faq.json`
-   **Outbreak Alerts:** `knowledge_base/outbreak_alerts.json`
-   **Vaccination Schedule:** `knowledge_base/vaccination_schedule.json`

These files can be updated to expand the chatbot's knowledge.

# Design Document: CognitiveDrift

## 1. System Architecture
The system follows a layered architecture consisting of a User Input Layer, an NLP Analysis Engine, and a Dashboard/Notification Layer.


## 2. Tech Stack
**Frontend:** React-based dashboard for data visualization (CSI Meter, Trend Graphs).
**Backend:** Python with FastAPI for high-performance API services.
**AI/ML:** AWS Bedrock for LLM integration and NLP analysis.
**Database:** PostgreSQL for secure storage of historical cognitive scores.

## 3. Component Design
**NLP Analysis Engine:** Processes writing behavior to analyze reasoning depth and idea diversity.
**Signal Detection Models:** Specific modules for Repetition Detection and Idea Diversity.
**CSI Calculation Module:** A logic layer that aggregates signals into a single numerical score (0-100).
**Alerting System:** Triggers notifications via the dashboard when the CSI drops below a certain threshold.

## 4. Data Flow
1. User interacts with the platform (writing/solving problems).
2. Interaction data is sent to the FastAPI backend.
3. AWS Bedrock analyzes the text for cognitive signals.
4. The CSI Module updates the user's score.
5. React Dashboard reflects the change in real-time[cite: 51, 58].

## 5. Ethical Design
* Data is anonymized before being processed by NLP models.
* No medical diagnoses are made; the focus is strictly on productivity and thinking patterns.

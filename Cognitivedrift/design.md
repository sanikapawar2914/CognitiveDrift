# Design Document: CognitiveDrift

## 1. System Architecture
[cite_start]The system follows a layered architecture consisting of a User Input Layer, an NLP Analysis Engine, and a Dashboard/Notification Layer[cite: 71, 72].


## 2. Tech Stack
* [cite_start]**Frontend:** React-based dashboard for data visualization (CSI Meter, Trend Graphs)[cite: 91, 93].
* [cite_start]**Backend:** Python with FastAPI for high-performance API services[cite: 90, 92].
* [cite_start]**AI/ML:** AWS Bedrock for LLM integration and NLP analysis[cite: 86, 88].
* [cite_start]**Database:** PostgreSQL for secure storage of historical cognitive scores[cite: 94, 95].

## 3. Component Design
* [cite_start]**NLP Analysis Engine:** Processes writing behavior to analyze reasoning depth and idea diversity[cite: 73, 78].
* [cite_start]**Signal Detection Models:** Specific modules for Repetition Detection and Idea Diversity[cite: 74, 75].
* [cite_start]**CSI Calculation Module:** A logic layer that aggregates signals into a single numerical score (0-100)[cite: 79].
* [cite_start]**Alerting System:** Triggers notifications via the dashboard when the CSI drops below a certain threshold[cite: 55, 80].

## 4. Data Flow
1. User interacts with the platform (writing/solving problems).
2. Interaction data is sent to the FastAPI backend.
3. AWS Bedrock analyzes the text for cognitive signals.
4. The CSI Module updates the user's score.
5. [cite_start]React Dashboard reflects the change in real-time[cite: 51, 58].

## 5. Ethical Design
* Data is anonymized before being processed by NLP models.
* [cite_start]No medical diagnoses are made; the focus is strictly on productivity and thinking patterns[cite: 24, 31].
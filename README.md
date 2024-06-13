# OJ-Online-Judge-
High-Level System Architecture
1. Frontend
User Interface: Provides users with a web interface to sign up, log in, browse problems, submit solutions, and view results.
Problem List: Displays a list of available problems with details such as problem statement, constraints, and sample inputs/outputs.
Submission Form: Allows users to submit their code solutions in various programming languages.
2. Backend
API Server: Handles requests from the frontend and coordinates with other backend services.
Authentication & Authorization: Manages user accounts and permissions.
Problem Management: Manages problem creation, updates, and retrieval.
Submission Management: Handles code submissions, stores them, and initiates the evaluation process.
Database: Stores user data, problem details, submission history, and evaluation results.
User Data: Information about users, such as usernames, passwords, and submission history.
Problem Data: Details of programming problems, including problem statements, test cases, and constraints.
Submission Data: Records of all submissions, including user ID, problem ID, submitted code, and evaluation results.
3. Code Evaluation System
Job Queue: Manages the queue of submitted code awaiting evaluation.
Sandbox Environment: A secure, isolated environment where code is compiled and executed to prevent security risks.
Compiler & Executor: Compiles and runs the submitted code in various programming languages.
Test Case Manager: Provides input to the code, captures the output, and compares it against expected results.
Result Evaluator: Determines the correctness of the code based on the test case results and assigns a status (e.g., Accepted, Wrong Answer, Runtime Error, Time Limit Exceeded).
4. Monitoring & Logging
Logging System: Records system events and user actions for debugging and auditing purposes.
Monitoring Tools: Tracks system performance and health metrics to ensure reliability and scalability.
Workflow
User Interaction:

User logs in and browses available problems.
User selects a problem and submits their code solution via the submission form.
Submission Handling:

The API server receives the submission and stores it in the database.
The submission is added to the job queue for evaluation.
Code Evaluation:

The code is picked up from the job queue and sent to the sandbox environment.
The code is compiled and executed against a set of predefined test cases.
The output of the code is compared with the expected results.
The result (e.g., Accepted, Wrong Answer) is recorded in the database.
Result Feedback:

The user is notified of the result through the frontend.
The user can view detailed feedback, including which test cases failed (if any).

# TeachersArch: Website for Predicting Student Outcomes Using GitLab Activity

This project, developed for the Data Science and Engineering Project course at the University of Coimbra, focuses on building a machine learning model to predict student performance in a software engineering course. The prediction is based on student activity data extracted from GitLab repositories, which serves as a proxy for engagement, collaboration, and productivity.

**Objective**
The primary goal is to develop a machine learning model that can predict student outcomes (such as final grades, pass/fail status, or performance tiers) by analyzing their version control and collaboration data from GitLab. The project culminates in a simple user interface to demonstrate the model's predictive capabilities.

**Problem Statement**

Software engineering courses heavily rely on collaborative coding projects hosted on platforms like GitLab. A student's activity on these platforms—including commits, merge requests, and issue tracking—can provide valuable insights into their participation, teamwork skills, and coding habits. By analyzing this data, we aim to build a predictive model that helps instructors identify students who may need additional support, thereby improving academic outcomes and providing actionable feedback.

**Project Milestones**

The project is structured into three distinct milestones, each with its own set of objectives and evaluation criteria.

- Milestone 1: Project Planning and Foundation

This initial phase focused on setting up the project's foundation, defining its scope, and structuring the work in GitLab.

- Use Cases & Quality Attributes: Correctly defined and documented all use cases and quality attributes within GitLab issues and wikis.
- Repository Structure: Established a consistent and logical repository structure to manage all project artifacts, including documentation, code, and data.
- Initial Documentation: Created foundational documents for architecture, requirements, and management.

- Milestone 2: Implementation and Integration
This milestone centered on developing the core application, integrating the various components, and ensuring robust testing.

- Test Case Development: Wrote and executed a comprehensive suite of test cases, all consistently defined in GitLab.
- Application Integration: Integrated the data collection, preprocessing, and modeling components into a single, cohesive application.
- Feature Demonstration: Prepared a demonstration of all implemented features, showcasing the progress and functionality of the integrated system.

Milestone 3: Final Model, Evaluation, and Demo
The final phase focused on finalizing the model, conducting a thorough analysis, and delivering a full demonstration of the project.

- End-to-End Use Case Validation: Ensured all use cases were correctly and sufficiently implemented.
- Quality Assurance: Validated that all defined quality attributes were met.
- Full System Demo: Produced a complete demonstration of the predictive model and its user interface in a single, unified environment.
- Individual Work Analysis: Conducted and documented individual analyses of the results and contributions.

**Technical Workflow**
The project follows a standard machine learning workflow, from data collection to model deployment.

- Data Sources
The model is built using two primary data sources:

GitLab Activity Data: Collected via the GitLab API, containing metrics on:
  - Commits: Number of commits, average lines of code added/removed, time distribution.
  - Merge Requests: Number of created and merged requests, review comments.
  - Issues: Number of issues created, assigned, and resolved; participation in discussions.
  - Branching: Number of branches created and merge frequency.
Student Grades: Provided as CSV files, containing midterm and final project grades.

- Data Preprocessing and Feature Engineering
Cleaning: Handled missing or incomplete data, such as from students who did not use GitLab consistently.
Feature Engineering: Generated meaningful features from raw GitLab data (e.g., "average commits per week," "active weeks").
Normalization & Aggregation: Scaled performance metrics for consistency and aggregated them on a per-student basis.

- Model Development
Based on the prediction task, we explored both classification and regression models:
  - Classification Models: Decision Tree, Random Forest, Gradient Boosting (XGBoost) to         predict pass/fail outcomes or performance tiers (high/medium/low).
  - Regression Models: Linear Regression, Neural Networks to predict final numerical grades.
 
- Evaluation
The models were evaluated using standard metrics:
  - For Classification: Accuracy, Precision, Recall, F1-Score, and ROC-AUC.
  - For Regression: Mean Absolute Error (MAE), Mean Squared Error (MSE), and R² Score.

**Tech Stack and Tools**
Version Control: GitLab (Mandatory)
Programming Language: Python
Data Manipulation and Analysis: Pandas, NumPy, Scikit-learn
GitLab API Interaction: python-gitlab
User Interface: React
Backend: Django REST 

**Repository Structure**
- Architecture: Contains all documents related to the system's design. This includes the Entity-Relationship (ER) Diagram, which models the database structure, and a detailed description of the 3-Tier Layered Architecture (Presentation, Application, and Data Layers) that guides the application's construction.
- Code: 

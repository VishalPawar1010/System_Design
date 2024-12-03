## Detailed Pipeline Stages with respect to real world project

![DevOps pipeline](./DevOps_example.png)

### Development Process

1. **User Story Creation**:

   - **Action**: The process starts with a product owner creating user stories based on requirements.

2. **Sprint Planning**:

   - **Action**: The dev team picks up the user stories from the backlog and puts them into a sprint for a two-week dev cycle.

3. **Source Code Management**:

   - **Action**: Developers commit source code into the code repository Git.

4. **Continuous Integration (CI)**:

   - **Build**:
     - **Action**: A build is triggered in Jenkins. The source code must pass unit tests, code coverage threshold, and gates in SonarQube.
     - **Details**: The build stage compiles the code, resolves dependencies, and packages the application, ensuring that the codebase remains in a deployable state.
   - **Test**:
     - **Action**: Automated tests are executed to verify code quality and functionality.
     - **Tools**: Unit tests, integration tests, and static code analysis tools.
     - **Best Practices**: Incorporate a comprehensive test suite to catch issues early and maintain high code quality standards.

5. **Artifact Storage**:

   - **Action**: Once the build is successful, the build is stored in Artifactory. Then the build is deployed into the dev environment.

6. **Independent Feature Testing**:

   - **Action**: There might be multiple dev teams working on different features. The features need to be tested independently, so they are deployed to QA1 and QA2.

7. **Quality Assurance (QA)**:

   - **Action**: The QA team picks up the new QA environments and performs QA testing, regression testing, and performance testing.

8. **User Acceptance Testing (UAT)**:

   - **Action**: Once the QA builds pass the QA team’s verification, they are deployed to the UAT environment.

9. **Production Release**:

   - **Action**: If the UAT testing is successful, the builds become release candidates and will be deployed to the production environment on schedule.

10. **Production Monitoring**:
    - **Action**: The SRE (Site Reliability Engineering) team is responsible for production monitoring.

A DevOps pipeline typically consists of several interconnected stages, each contributing to the seamless delivery of software from development to production

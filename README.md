
# JenkinsMaster Job DSL Configuration

This repository contains Job DSL scripts for configuring pipeline jobs in Jenkins for the **JenkinsMaster** setup. It provides a structured setup to define backend and frontend pipelines within a dedicated `HelloWorld` folder, supporting reusable and modular configurations.

## Repository Structure

- **folders/**: Contains definitions for organizing jobs within a specific folder.
  - `helloworld.yml`: Creates the `HelloWorld` folder as a logical container for jobs.
- **jobs/**: Contains Job DSL scripts to define Jenkins jobs.
  - `helloworld-backend.yml`: Defines the backend pipeline job.
  - `helloworld-frontend.yml`: Defines the frontend pipeline job.

## Requirements

- **Jenkins** with **Job DSL** and **Configuration as Code (CASC)** plugins installed.
- CASC plugin configured to load `.yml` files from this repository for creating jobs.

## Setup

1. **Clone or Fork this Repository**
   ```bash
   git clone https://github.com/mamrezb/jenkinsmaster-job-dsl.git
   ```

2. **Add Repository to CASC Configuration**
   No specific configuration path is needed as Jenkins CASC plugin will automatically load all `.yml` files.

3. **Folder and Jobs Loading**
   - The `HelloWorld` folder is created first, followed by `Backend` and `Frontend` pipeline jobs to maintain organization.
   - Jobs are created under `HelloWorld` as specified in the respective job files.

4. **Customize Jobs**
   Modify the `.yml` files in the `folders/` and `jobs/` directories to add, adjust, or configure additional jobs.

## Folder and Jobs Defined

### HelloWorld Folder

A logical container in Jenkins for organizing example jobs.

- **Backend Pipeline** (`HelloWorld/Backend`)
  - A pipeline job for backend applications.
  - Uses a Git repository with a `Jenkinsfile` for pipeline definition.
  - Repository URL: [jenkinsmaster-backend-hello-world](https://github.com/mamrezb/jenkinsmaster-backend-helloworld)

- **Frontend Pipeline** (`HelloWorld/Frontend`)
  - A pipeline job for frontend applications.
  - Uses a Git repository with a `Jenkinsfile` for pipeline definition.
  - Repository URL: [jenkinsmaster-frontend-hello-world](https://github.com/mamrezb/jenkinsmaster-frontend-helloworld)

## Contributing

Contributions are welcome! Feel free to submit pull requests to add more example jobs, improve configurations, or add features.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
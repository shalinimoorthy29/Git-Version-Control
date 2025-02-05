# Git Version Control Mini-Project

This mini-project showcases the use of Git version control on Windows using Windows Subsystem for Linux (WSL). It demonstrates the steps for setting up Git, creating an SSH authentication key, and performing basic Git operations such as initializing a repository, adding files, committing changes, and pushing to a remote repository.

## Project Overview

The purpose of this project is to document my experience with Git version control and demonstrate my ability to:

- Set up Git on WSL for Windows.
- Configure SSH authentication for secure communication with GitHub.
- Use basic Git commands to manage a project repository.

## Steps Performed

### 1. Installing WSL and Git
```bash
# Install WSL
wsl --install (Following this ubuntu distribution was automatically installed)

# Update and upgrade the system
sudo apt update && sudo apt upgrade

# Install Git
sudo apt-get install git
```

### 2. Setting Up SSH Authentication
```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your.email@example.com"

# Add SSH key to the agent
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_ed25519

# Copy the public key and add it to GitHub
cat ~/.ssh/id_ed25519.pub
```

### 3. Initializing the Repository
```bash
# Navigate to the project directory
cd /mnt/c/Users/shali/Documents/L\&D/GitHub\ Projects

# Create a new directory for the project
mkdir Git-Version-Control
cd Git-Version-Control

# Initialize Git repository
git init
```

### 4. Adding Files and Committing Changes
```bash
# Create a directory for the project files
mkdir "001_cBioPortal_Pediatric AML TARGET 2018"

# Add files to the repository
git add "001_cBioPortal_Pediatric AML TARGET 2018/*"

# Commit the changes
git commit -m "Initial commit: Add Jupyter notebook and data files for Paediatric AML project"
```

### 5. Connecting to Remote Repository and Pushing Changes
```bash
# Add the remote repository
git remote add origin git@github.com:shalinimoorthy29/Git-Version-Control.git

# Push changes to the remote repository
git push -u origin master
```

## Files in the Repository

- **Pediatric Acute Myeloid Leukemia TARGET 2018.ipynb**: Jupyter Notebook for the project analysis.
- **aml_target_2018_pub_clinical_data.tsv**: Raw clinical data in TSV format.
- **aml_target_2018_pub_clinical_data.xlsx**: Raw clinical data in Excel format.

## Key Takeaways

This project highlights the following skills:

- Configuring Git and SSH on WSL for secure communication.
- Initializing and managing a local Git repository.
- Performing Git operations such as adding, committing, and pushing changes.

## Repository Structure
```
Git-Version-Control/
├── 001_cBioPortal_Pediatric AML TARGET 2018/
│   ├── Pediatric Acute Myeloid Leukemia TARGET 2018.ipynb
│   ├── aml_target_2018_pub_clinical_data.tsv
│   └── aml_target_2018_pub_clinical_data.xlsx
```

## Future Enhancements

- Demonstrate advanced Git workflows, such as branching and merging.




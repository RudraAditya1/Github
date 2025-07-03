# GitHub Clone – Custom Version Control System

A full-fledged clone of GitHub featuring user authentication, repository management, a custom-built version control system, and a responsive UI inspired by GitHub.

---

## 🔥 Features

* **User Authentication:** Login/Signup functionality with encrypted credentials.
* **Profile Page:** Displays user information and a list of repositories.
* **Repositories:** Create, update, delete, and manage repositories with metadata.
* **Custom Git Commands:** Implements a version control system with commands like `init`, `add`, `commit`, and `log` via Node.js.
* **Dark/Light Mode:** Toggle theme for better UI/UX experience.
* **GitHub UI Clone:** Replicated GitHub's frontend for familiar navigation and layout.
* **AWS Integration for File Storage:** Commits are stored securely on AWS. Each commit is assigned a **unique ID generated using UUID v4**. Files can be **pushed to AWS** and **retrieved using `node index.js revert <unique_id>`**. This allows recovery of accidentally deleted files by referencing the unique commit folder.

---

## 🚀 Tech Stack

* **Frontend:** HTML, CSS, JavaScript, React.js
* **Backend:** Node.js, Express.js
* **Database:** MongoDB
* **Cloud:** AWS S3 (for storing commit snapshots)

---

## ⚙️ Setup Instructions

### Prerequisites:

* Node.js installed
* MongoDB running locally or via Atlas
* Git (for your own project tracking)

### Steps to Run Locally:

```bash
# Clone the repository
$ git clone https://github.com/YourUsername/github-clone.git

# Navigate to project directory
$ cd github-clone

# Install dependencies
$ npm install

# Start the development server
$ npm start
```

### Run Frontend (If separated):

```bash
# Navigate to frontend directory
$ cd client

# Install dependencies
$ npm install

# Start React app
$ npm run dev
```

---

## 💻 Custom Git Commands (via Node.js)

Your custom version control system is invoked through:

```bash
# Initialize a new repo
$ node index.js init

# Add files to staging
$ node index.js add <filename>

# Commit changes
$ node index.js commit -m "commit message"

# View commit history
$ node index.js log

# Push committed files to AWS (generates UUID and folder)
$ node index.js push

# Pull files from AWS (basic fetch)
$ node index.js pull

# Revert deleted files using UUID
$ node index.js revert <unique_id>
```

> All versioning data is saved locally in a custom `.vcs` directory and remotely on AWS, mimicking Git functionality with cloud redundancy and restore capability.

---

## 📂 Project Structure

```text
├── client/                # React frontend
├── server/                # Node.js + Express backend
├── index.js               # Command-line tool for version control
├── .vcs/                  # Custom version control storage
├── README.md
```

---

## 🧪 Future Enhancements

* Branching and merging
* Pull/push features with version diffs
* Open-source collaboration workflow
* Enhanced conflict resolution strategies

---

## 📫 Contact

Created by **Rudra Aditya**
LinkedIn: [linkedin.com/in/ra63](https://www.linkedin.com/in/ra63)
GitHub: [github.com/RudraAditya1](https://github.com/RudraAditya1)

Feel free to star ⭐ the repo if you find it helpful!

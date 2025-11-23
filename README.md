# 💻 PyRun Host — Mini Web Python IDE

A lightweight, publicly hostable **Mini Web IDE** that allows users to write and execute Python code directly in their browser using **Pyodide**.

This project is specifically designed to be easily hosted on platforms like GitHub Pages or Netlify, offering a safe, sandboxed environment for educational or simple script-running purposes.

## ✨ Features

* **In-Browser Execution:** Runs standard Python code directly in the user's browser via the Pyodide WebAssembly runtime.
* **Zero Backend Required:** The entire application is a single HTML file with no server-side dependencies, making it ideal for free static hosting.
* **Client-Side Persistence:** Code and open tabs are automatically saved to the browser's local storage every 2 seconds.
* **Multi-File Tabs:** Supports creating and managing multiple Python files (`.py`) within the IDE environment.
* **Package Management:** Includes support for installing compatible Python packages (e.g., NumPy, Pandas) using `micropip`.
* **Utility Tools:** Features include code formatting (using `black`), adjustable execution timeout (default 20s), and a set of built-in demo examples.
* **Safe & Private:** Files are stored *only* in the user's browser, ensuring privacy and preventing device filesystem access.

## 🚀 How to Use

The IDE is intuitive, similar to desktop coding environments.

### Running Code

1.  Write your Python code in the active editor tab.
2.  Click the **`Run ▶`** button or press **`Ctrl/Cmd + Enter`**.
3.  The output (stdout, stderr, and result) will appear in the **Output** panel on the right.

### Installing Packages

1.  In the **Packages (micropip)** section, enter the names of the packages you need (e.g., `numpy pandas`).
2.  Click the **`Install`** button. Pyodide will fetch and install the packages for the current session.

### Managing Files

* **Saving:** Code is auto-saved to your browser.
* **Download:** Click the **`Download`** button to save the current file as a `.py` file to your computer.
* **Upload:** Click **`Upload`** to load a local `.py` or text file into a new tab in the IDE.

## ⚙️ Project Structure & Technology

The entire application is contained within the `index.html` file (formerly `pyrun_pro_host.html`).

* **Runtime:** Pyodide
* **Editor:** CodeMirror (v5.65.13)
* **Styling:** Minimal custom CSS with the CodeMirror `material-darker` theme.
* **Data Storage:** Uses the browser's `localStorage` to save user project data under the key `pyrun_project_v1`.

## 🌐 Public Hosting (For Developers)

To host your own version of this IDE:

1.  Create a new public GitHub repository.
2.  Commit the `index.html` file (or `pyrun_pro_host.html`).
3.  Enable **GitHub Pages** from the repository **Settings**, selecting the `main` branch and the `/ (root)` folder as the source.

The IDE will be live at `https://<YourUsername>.github.io/<YourRepoName>/`.

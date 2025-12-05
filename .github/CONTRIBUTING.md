# Contributing to WebScrape-Email-Social-Extractor-Ruby-CLI

Thank you for considering contributing to `WebScrape-Email-Social-Extractor-Ruby-CLI`! We aim to maintain a professional, high-velocity, and zero-defect project, following the **Apex Technical Authority** standards.

## 1. Code of Conduct

This project adheres to the Contributor Covenant Code of Conduct. By participating, you are expected to uphold this code. Please report any violations to `chirag127@example.com`.

## 2. Core Principles

*   **Zero-Defect:** Strive for the highest quality code. All contributions must pass rigorous automated checks.
*   **High-Velocity:** Efficient workflows and clear contribution guidelines enable rapid development.
*   **Future-Proof:** Embrace modern practices and ensure maintainability.
*   **Professional Archival Standard:** Even experimental or retired code should be well-documented and maintainable.

## 3. Getting Started

1.  **Fork the Repository:** Create your own fork of the `chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI` repository.
2.  **Clone Your Fork:** Clone your forked repository to your local machine.
    bash
    git clone https://github.com/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI.git
    cd WebScrape-Email-Social-Extractor-Ruby-CLI
    
3.  **Setup Development Environment:** Ensure you have Ruby 3.0+ and Bundler installed.
    bash
    # Install dependencies
    bundle install
    

## 4. Contribution Workflow

1.  **Create a New Branch:** Start a new branch for your feature or bug fix. Use a descriptive name (e.g., `feature/add-advanced-filtering` or `fix/serpapi-auth-issue`).
    bash
    git checkout -b your-branch-name
    
2.  **Make Your Changes:** Write clean, well-commented Ruby code. Follow existing style conventions.
3.  **Add Tests:** All new features must be accompanied by relevant unit or integration tests. Ensure existing tests are passing.
4.  **Lint and Format:** Use `RuboCop` (configured in `.rubocop.yml`) to ensure code quality and consistency. `bundle exec rubocop -a` will auto-correct many issues.
5.  **Commit Your Changes:** Make clear, concise commit messages.
    bash
    git add .
    git commit -m "feat: Add new feature for extracting LinkedIn profiles"
    
6.  **Push to Your Fork:** Push your branch to your fork on GitHub.
    bash
    git push origin your-branch-name
    
7.  **Open a Pull Request:** Submit a Pull Request from your branch to the `main` branch of the `chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI` repository.

## 5. Pull Request Guidelines

*   **Clear Description:** Explain what your PR does, why it's needed, and how you've tested it.
*   **Link to Issues:** If your PR addresses an issue, reference it using `#issue-number`.
*   **Target Branch:** Ensure your PR targets the `main` branch.
*   **CI/CD:** All automated checks (CI/CD pipeline, linting, testing) must pass before your PR can be merged.

## 6. Technical Stack & Architecture

*   **Language:** Ruby 3.0+
*   **Package Manager:** Bundler
*   **Core Libraries:** `Nokogiri` (for HTML parsing), `HTTParty` or `Faraday` (for HTTP requests), `google-search-results` (for SerpApi integration).
*   **Linting/Formatting:** `RuboCop` (with standard configuration).
*   **Testing:** `RSpec`.
*   **Architecture:** Adheres to standard CLI application patterns. Focus on modularity and testability, especially in the scraping and data extraction logic.

## 7. Reporting Issues

When reporting an issue, please include:

*   A clear, concise title.
*   The version of Ruby and the gem you are using.
*   Steps to reproduce the bug.
*   Expected behavior vs. actual behavior.
*   Any relevant error messages or screenshots.

## 8. Feature Requests

If you have an idea for a new feature, please open an issue first to discuss it. This helps us ensure alignment and prioritize development.

---

*This document is dynamically managed by the Apex Technical Authority.*

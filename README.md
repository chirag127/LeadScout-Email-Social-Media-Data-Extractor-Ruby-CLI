# WebScrape-Email-Social-Extractor-Ruby-CLI

[![Build Status](https://img.shields.io/github/actions/workflow/user/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI/ci.yml?style=flat-square&logo=githubactions)](https://github.com/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI?style=flat-square&logo=codecov)](https://codecov.io/gh/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI)
[![Ruby Version](https://img.shields.io/ruby/v/web-scrape-email-social-extractor-ruby-cli?style=flat-square)](https://rubygems.org/gems/web-scrape-email-social-extractor-ruby-cli)
[![License](https://img.shields.io/github/license/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI?style=flat-square)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI?style=flat-square)](https://github.com/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI/stargazers)

## Blazing Fast Web Scraping for Lead Generation

This Ruby CLI tool efficiently extracts email addresses, social media handles, and other crucial information from websites by leveraging Google Search Results via SerpApi, empowering targeted lead generation.

## Architecture Diagram

mermaid
graph TD
    A[User Input: Target URL/Query] --> B{CLI Interface}
    B --> C[SerpApi Integration]
    C --> D[Google Search Results Parsing]
    D --> E[Information Extraction Module]
    E --> F[Email Extraction]
    E --> G[Social Media Handle Extraction]
    E --> H[Other Data Points]
    F --> I{Output Data}
    G --> I
    H --> I
    I --> J[Formatted Output (CSV/JSON)]
    J --> K[Lead Generation Database/CRM]


## Table of Contents

*   [Architecture Diagram](#architecture-diagram)
*   [Table of Contents](#table-of-contents)
*   [AI Agent Directives](#ai-agent-directives)
*   [Features](#features)
*   [Installation](#installation)
*   [Usage](#usage)
*   [Development](#development)
    *   [Running Tests](#running-tests)
    *   [Code Style](#code-style)
*   [Contributing](#contributing)
*   [License](#license)

## AI Agent Directives

<details>
<summary><strong>🤖 APEX AI AGENT DIRECTIVES (DECEMBER 2025 EDITION)</strong></summary>

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** Detect the project type and apply the corresponding **Apex Toolchain**.

*   **PRIMARY SCENARIO: SYSTEMS / PERFORMANCE (Ruby / Go / Rust)**
    *   **Stack:** This project leverages **Ruby 3.3+**. Key tools include **Bundler** (for package management), **RuboCop** (for strict linting and formatting), and **RSpec** (for robust unit and integration testing).
    *   **Architecture:** Adheres to a **Modular Monolith** pattern, ensuring clear separation of concerns for features like SerpApi integration, data parsing, and CLI interface, while maintaining a unified deployment. 
    *   **External Services:** Integration with **SerpApi** for search result fetching. Prioritize robust error handling, rate limiting considerations, and secure API key management.
    *   **CLI Framework:** Uses `Thor` or `Commander` for a powerful and intuitive command-line interface.

---

## 4. ARCHITECTURE & QUALITY MANDATES
*   **SOLID Principles:** Adhere strictly to SOLID principles for maintainable and scalable code.
*   **DRY (Don't Repeat Yourself):** Eliminate redundant code through effective abstraction.
*   **KISS (Keep It Simple, Stupid):** Favor straightforward solutions.
*   **YAGNI (You Aren't Gonna Need It):** Implement only necessary features.
*   **Error Handling:** Implement comprehensive error handling, logging, and graceful degradation.
*   **Security:** Implement security best practices, including secure handling of API keys and input sanitization.
*   **Testing:** Maintain a minimum of **90% code coverage** through comprehensive unit and integration tests.

---

## 5. DEVELOPMENT LIFECYCLE STANDARDS
*   **Version Control:** Use Git with a clear branching strategy (e.g., Gitflow).
*   **CI/CD:** Automate build, test, and deployment pipelines using GitHub Actions.
*   **Documentation:** Maintain up-to-date documentation, including READMEs, inline code comments, and architectural diagrams.

</details>

## Features

*   Scrapes email addresses from Google Search Results.
*   Extracts social media profile links (LinkedIn, Twitter, etc.).
*   Configurable output formats (e.g., CSV, JSON).
*   Utilizes SerpApi for reliable access to Google Search.
*   Intuitive command-line interface.

## Installation

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI.git
    cd WebScrape-Email-Social-Extractor-Ruby-CLI
    

2.  **Install dependencies:**
    bash
    bundle install
    

3.  **Configure API Key:**
    Create a `.env` file in the root of the project and add your SerpApi API key:
    dotenv
    SERPAPI_API_KEY=YOUR_SERPAPI_API_KEY
    
    Alternatively, set it as an environment variable before running the script.

## Usage

Run the CLI tool with your desired search query or target URL.

bash
./bin/scrape_data --query "best digital marketing agencies in New York"


bash
./bin/scrape_data --url "https://example.com/search-results-page"


**Options:**

*   `--query <search_term>`: The search query to use on Google.
*   `--url <web_url>`: A specific URL to scrape.
*   `--output <format>`: Output format (`csv` or `json`, defaults to `csv`).
*   `--limit <number>`: Limit the number of search results to process.

## Development

### Running Tests

This project uses RSpec for testing. To run the test suite:

bash
bundle exec rspec


### Code Style

This project adheres to Ruby best practices enforced by RuboCop. To check code style:

bash
bundle exec rubocop


To auto-correct style issues:

bash
bundle exec rubocop -a


## Contributing

Contributions are welcome! Please read our [CONTRIBUTING.md](CONTRIBUTING.md) file for details on how to submit pull requests and report issues.

## License

This project is licensed under the CC BY-NC license. See the [LICENSE](LICENSE) file for more details.

🛡️ CERBERE-Smart-Security-Auditor

CERBERE-Smart-Security-Auditor is a lightweight, ultra-fast, and 100% offline security analysis and code auditing tool. It allows you to analyze software projects using an extensive framework of 235 security checks, covering modern web vulnerabilities, smart contracts, systems code, and autonomous AI agents.

✨ Key Features
235 Security Checks: Comprehensive coverage ranging from traditional web vulnerabilities (OWASP Top 10) to modern architectures.
100% Local & Offline: No data, files, or source code leave your browser during local analysis.
Hybrid Detection Engine:
Detection based on the presence or absence of patterns or specific filenames.
Advanced conditional mode (e.g., detecting a swap() call without a deadline parameter).
Native support for .html, .js, .jsx, .ts, .tsx, .rs, .go, .sol, and other file extensions.
163 of the 235 checks in the framework are automated.
Instant FR / EN Translation: Switch the interface and security framework between French and English with a single click (top-right corner), without losing the security score or the current analysis state.
Anthropic AI Assistant (Optional): Direct integration with Claude to perform deeper analysis and ask questions about detected vulnerabilities.
🔍 Security Framework (235 Checks)

The framework incorporates the latest identified vulnerabilities, including findings informed by ECC-main field reports:

Advanced Frontend (React / Next.js): dangerouslySetInnerHTML sanitization, validation of javascript:/data: URIs, target="_blank" protections, Zod validation for Server Actions, NEXT_PUBLIC_* secret exposure, and httpOnly cookies.
Rust: Hardcoded secret detection, SQL injection through format!, undocumented unsafe blocks, missing cargo audit checks, and explicit client-side error handling.
Go: Secure handling of os.Getenv and explicit network timeouts using context.WithTimeout.
DeFi & Smart Contracts (Solidity): Reentrancy attacks (Checks-Effects-Interactions, or CEI), vault inflation attacks, manipulable spot oracles (requiring TWAP), swaps without slippage protection or a deadline, transfer calls without SafeERC20, and administrative functions without onlyOwner access control.
Autonomous AI Trading Agents: Hardcoded spending limits, pre-transaction simulations (dry runs), circuit breakers, hardcoded wallet private keys, MEV protection, and prompt-injection validation.
Cross-Cutting Security Enhancements: Security headers (Permissions-Policy, Referrer-Policy, and CSP without unsafe-inline), JWT validation (audience/issuer), and sensitive data leakage through structured logs.
🚀 Installation & Quick Start

No complex installation, Node.js server, or Docker container is required.

1. Download the project
git clone https://github.com/mikateproduction-wq/Cerbere_auditeur.git
cd Cerbere_auditeur
2. Launch the application

Simply double-click the cerbere-auditeur.html file to open it in your web browser (Chrome, Firefox, Edge, Brave, or Safari).

🤖 Configuring the Anthropic AI Assistant

Cerbère includes direct client-side integration with the Anthropic API to help you remediate vulnerabilities.

Activation
In the interface, open the AI Assistant panel.
Enter your Anthropic API key (sk-ant-...).
Choose your model:
Claude Sonnet (Recommended: balanced speed and analytical depth)
Claude Opus (For highly complex analyses)
Claude Haiku (For ultra-fast responses)
Click Save. A live verification ping checks the validity of your API key against api.anthropic.com.

Technical Note: API requests are made directly using fetch, with the anthropic-dangerous-direct-browser-access: true header. Your API keys remain stored exclusively in your browser's local storage (LocalStorage) and are not sent to any third-party server. If the connection is lost, the tool automatically falls back to its local analysis engine.

📖 User Guide

File Selection: Drag and drop your project folder or individual files into the analysis area.

Start the Audit: The analysis runs instantly and locally.

Review the Report:

View the overall security score.
Filter findings by vulnerability category or severity level.
Review the extracted code evidence for each detected issue.

Export: Export your report in JSON or Markdown format to share it with your team.

🔒 Privacy & Security

Zero Telemetry: Your source code files are never sent to a remote server.

API Key Security: The Anthropic API key is optional and remains strictly confidential within your browser.

For questions, support requests, or suggestions regarding Cerbère, feel free to contact us or join us through the various channels listed on our GitHub page.

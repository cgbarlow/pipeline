# Shameless vibe-coding CI/CD pipeline
High-level details of the current development pipeline I'm using. Expect this to evolve as tweaks and improvements are made.

```mermaid
graph LR
    A[Visual Studio Code]
    B[GitHub Codespace]
    C["GitHub Repository"]
    D["Roo Code (VS Code Extension)"]
    E["Cline Recursive Chain of Thought System"]
    F[GitHub Copilot Pro]
    G["Anthropic Claude Sonnet 3.5"]
    H["Netlify (CI/CD Deployment)"]

    A --> B
    B -->|Push Code| C
    D --> A
    E --> D
    F --> D
    G --> F
    C -->|Triggers Build| H
```

## Components
### Visual Studio Code
- Our code editor - https://code.visualstudio.com/

### GitHub
- Code repository - https://github.com/

### GitHub Codespace
- Cloud-based IDE - https://code.visualstudio.com/docs/remote/codespaces

### Roo Code
- Autonomous coding agent (visual studio code extension) - https://marketplace.visualstudio.com/items?itemName=RooVeterinaryInc.roo-cline

### Cline Recursive Chain of Thought System
- System prompt for roo, essentially "memory" providing dynamic context for code changes - https://github.com/RPG-fan/Cline-Recursive-Chain-of-Thought-System-CRCT-

### Github Copilot Pro
- Monthly subscription providing access to a range of language models - https://github.com/features/copilot/plans?cft=copilot_li.features_copilot

### Anthropic Claude Sonnet 3.5
- Coding model of choice. Running through Github Copilot Pro - https://claude.ai/

### Netlify
- CI/CD deployment target. Hosts our website, provides continuous deployment on code commit - https://www.netlify.com/

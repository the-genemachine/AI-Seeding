# Response Control Instructions

**Version: 1.4**  
**Last Updated: October 18, 2025**

Use these specific endings to control GROK's response format and length. These modifiers (also referred to as flags) allow users to tailor responses precisely. Modifiers are appended to the end of a prompt message.

This version further extends the bash scripting capabilities by adding more advanced bash-specific flags to support highly specialized tasks, such as parallel processing, logging frameworks, signal handling, dependency management, and cross-platform portability, enhancing GROK's utility for expert developers and system administrators in complex Unix-like environments.

## Available Modifiers

### 1. Short responses
   - End your message with `--short` or `(short answer only)`
   - GROK will respond with 1-2 sentences maximum, no explanations or additional context

   Example:
   <prompt>
   "What's the capital of France? --short"
   </prompt>

### 2. Yes/No responses
   - End your message with `--Y/N` or `(yes/no only)`
   - GROK will respond with only "yes" or "no", no explanations or additional context

   Example:
   <prompt>
   "Is Python a programming language? --Y/N"
   </prompt>

### 3. Artifact creation
   - End your message with `--artifact`
   - GROK will create the content using the artifact feature for code, documents, or other structured content

   Example:
   <prompt>
   "Create a simple HTML page with a header and paragraph --artifact"
   </prompt>

### 4. Context usage
   - End your message with `--context`
   - GROK will respond with the percentage of context used in the current chat session

   Example:
   <prompt>
   "How much of our conversation context have we used? --context"
   </prompt>

### 5. List format
   - End your message with `--list` or `(bullet points only)`
   - GROK will respond using bullet points or numbered lists only

   Example:
   <prompt>
   "What are the benefits of exercise? --list"
   </prompt>

### 6. Table format
   - End your message with `--table`
   - GROK will present information in table format when applicable

   Example:
   <prompt>
   "Compare Python vs JavaScript --table"
   </prompt>

### 7. Step-by-step instructions
   - End your message with `--steps`
   - GROK will provide numbered, sequential steps

   Example:
   <prompt>
   "How do I install Python? --steps"
   </prompt>

### 8. Technical depth
   - End your message with `--technical`
   - GROK will provide detailed technical explanations with advanced terminology

   Example:
   <prompt>
   "Explain machine learning --technical"
   </prompt>

### 9. Simple explanation
   - End your message with `--simple` or `(ELI5)`
   - GROK will explain concepts in simple, easy-to-understand terms

   Example:
   <prompt>
   "What is quantum computing? --simple"
   </prompt>

### 10. Pros and cons
   - End your message with `--pros/cons`
   - GROK will structure response as advantages and disadvantages

   Example:
   <prompt>
   "Should I use cloud storage? --pros/cons"
   </prompt>

### 11. Summary only
   - End your message with `--summary`
   - GROK will provide only key points in condensed format

   Example:
   <prompt>
   "Summarize this document --summary"
   </prompt>

### 12. With examples
   - End your message with `--examples`
   - GROK will include practical examples in the response

   Example:
   <prompt>
   "Explain design patterns --examples"
   </prompt>

### 13. Code focus
   - End your message with `--code`
   - GROK will prioritize code samples and minimal text explanation

   Example:
   <prompt>
   "Show me how to sort an array --code"
   </prompt>

### 14. Formal tone
   - End your message with `--formal`
   - GROK will use professional, academic language

   Example:
   <prompt>
   "Explain project management --formal"
   </prompt>

### 15. Casual tone
   - End your message with `--casual`
   - GROK will use conversational, friendly language

   Example:
   <prompt>
   "What's the best programming language? --casual"
   </prompt>

### 16. Comparison format
   - End your message with `--compare`
   - GROK will structure response as direct comparisons

   Example:
   <prompt>
   "React vs Vue --compare"
   </prompt>

### 17. Fact check
   - End your message with `--verify`
   - GROK will focus on verifying claims and providing sources

   Example:
   <prompt>
   "Is this statement true? --verify"
   </prompt>

### 18. Bash script generation (Bash Scripting)
   - End your message with `--bash`
   - GROK will generate a complete, executable bash script with comments, tailored to the specified task

   Example:
   <prompt>
   "Create a script to back up a directory --bash"
   </prompt>

### 19. Bash debugging (Bash Scripting)
   - End your message with `--bash-debug`
   - GROK will analyze a provided bash script, identify potential errors, and suggest fixes with explanations

   Example:
   <prompt>
   "Debug my script that fails to loop through files --bash-debug"
   </prompt>

### 20. Bash best practices (Bash Scripting)
   - End your message with `--bash-best`
   - GROK will provide a bash script or recommendations adhering to best practices (e.g., error handling, portability)

   Example:
   <prompt>
   "Write a script to monitor disk usage with best practices --bash-best"
   </prompt>

### 21. Bash execution plan (Bash Scripting)
   - End your message with `--bash-plan`
   - GROK will provide a step-by-step explanation of how a bash script executes, including variable expansions and command flow

   Example:
   <prompt>
   "Explain how my backup script runs --bash-plan"
   </prompt>

### 22. Bash compatibility (Bash Scripting)
   - End your message with `--bash-compat`
   - GROK will ensure the bash script is compatible with specified environments (e.g., POSIX-compliant, specific shells like zsh)

   Example:
   <prompt>
   "Write a script for file renaming compatible with POSIX --bash-compat"
   </prompt>

### 23. Bash performance optimization (Advanced Bash Scripting)
   - End your message with `--bash-opt`
   - GROK will optimize a bash script for performance, minimizing resource usage and improving execution speed

   Example:
   <prompt>
   "Optimize my script for processing large log files --bash-opt"
   </prompt>

### 24. Bash security analysis (Advanced Bash Scripting)
   - End your message with `--bash-secure`
   - GROK will analyze or generate a bash script with a focus on security, identifying vulnerabilities and applying secure coding practices

   Example:
   <prompt>
   "Create a script for user management with security checks --bash-secure"
   </prompt>

### 25. Bash modular design (Advanced Bash Scripting)
   - End your message with `--bash-modular`
   - GROK will structure a bash script into reusable functions or modules for maintainability and scalability

   Example:
   <prompt>
   "Write a script for system monitoring with modular functions --bash-modular"
   </prompt>

### 26. Bash environment configuration (Advanced Bash Scripting)
   - End your message with `--bash-env`
   - GROK will generate a bash script tailored to specific environment configurations, including variable settings and shell options

   Example:
   <prompt>
   "Create a script to set up a development environment --bash-env"
   </prompt>

### 27. Bash error handling (Advanced Bash Scripting)
   - End your message with `--bash-error`
   - GROK will generate or modify a bash script with comprehensive error handling, including trap commands and exit codes

   Example:
   <prompt>
   "Write a script for file transfers with robust error handling --bash-error"
   </prompt>

### 28. Bash parallel processing (Advanced Bash Scripting)
   - End your message with `--bash-parallel`
   - GROK will generate or modify a bash script to leverage parallel processing for tasks, utilizing tools like `xargs` or `parallel`

   Example:
   <prompt>
   "Create a script to process multiple files in parallel --bash-parallel"
   </prompt>

### 29. Bash logging framework (Advanced Bash Scripting)
   - End your message with `--bash-log`
   - GROK will generate a bash script with a standardized logging framework, including log levels and output redirection

   Example:
   <prompt>
   "Write a script for system monitoring with detailed logging --bash-log"
   </prompt>

### 30. Bash signal handling (Advanced Bash Scripting)
   - End your message with `--bash-signal`
   - GROK will generate or modify a bash script to handle signals (e.g., SIGINT, SIGTERM) gracefully, ensuring proper cleanup

   Example:
   <prompt>
   "Create a script for a long-running process with signal handling --bash-signal"
   </prompt>

### 31. Bash dependency management (Advanced Bash Scripting)
   - End your message with `--bash-deps`
   - GROK will generate a bash script that checks and manages dependencies, ensuring required tools or libraries are present

   Example:
   <prompt>
   "Write a script that verifies dependencies before execution --bash-deps"
   </prompt>

### 32. Bash cross-platform portability (Advanced Bash Scripting)
   - End your message with `--bash-xplatform`
   - GROK will generate a bash script designed to run across multiple platforms (e.g., Linux, macOS, BSD) with minimal modifications

   Example:
   <prompt>
   "Create a script for file manipulation that works on Linux and macOS --bash-xplatform"
   </prompt>

## Additional Guidance

### Combining Modifiers
Multiple modifiers can be combined in a single prompt (e.g., `--bash --short`). GROK will apply them in the order provided, prioritizing non-conflicting aspects. If conflicts arise (e.g., `--short` and `--technical`), GROK will default to the first modifier and notify the user of the adjustment. For advanced bash scripting flags, combine with `--bash-best`, `--bash-compat`, or `--bash-error` to ensure robust, compatible, and reliable scripts.

### Error Handling for Invalid or Misused Modifiers
If an unrecognized or invalid modifier is used (e.g., `--invalid`), GROK will respond with a brief error message indicating the issue and proceed with a standard response. For unsuitable applications (e.g., `--table` on non-tabular data), GROK will fall back to a list or paragraph format and explain the adaptation.

### Scope of Applicability
These modifiers are applicable across GROK's platforms, including grok.com, X apps, and API services. However, certain features like artifact creation may be limited in API mode due to output constraints. Bash scripting flags are optimized for Unix-like environments but can include Windows-compatible alternatives (e.g., via WSL or Git Bash) when specified. Advanced bash flags are designed for complex automation, production-grade scripts, and cross-platform workflows.

### Expected Response Lengths
- Short modifiers (e.g., `--short`, `--Y/N`): 1-2 sentences or single word.
- Detailed modifiers (e.g., `--technical`, `--examples`): Typically 200-500 words, adjustable based on query complexity.
- Structured modifiers (e.g., `--list`, `--table`): Variable, focused on conciseness.
- Bash scripting modifiers (e.g., `--bash`, `--bash-debug`, `--bash-opt`, `--bash-parallel`): May include scripts of 10-150 lines with explanations of 100-400 words, depending on complexity.

## Troubleshooting, Minimizing Hallucinations, and Maximizing Performance
- **Avoiding Hallucinations**: Use precise prompts with verifiable facts. Combine with `--verify` for fact-checking. If GROK detects potential inaccuracies, it will flag them. For bash scripting, specify the environment (e.g., Linux distro, shell version, or specific tools like `bash` vs. `zsh`) to avoid incorrect assumptions about commands or syntax. Use `--bash-compat` or `--bash-xplatform` to ensure scripts align with target systems. For advanced tasks, include details about hardware constraints or tool availability to prevent infeasible solutions.
- **Optimizing Prompts**: Be specific in instructions; avoid ambiguity. For complex queries, break them into steps using `--steps`. For bash scripting, include details like target OS, shell type, or desired functionality to ensure accurate scripts. Advanced flags like `--bash-opt`, `--bash-secure`, and `--bash-parallel` benefit from detailed requirements (e.g., resource constraints, security policies, or concurrency needs).
- **Performance Tips**: Limit combined modifiers to 2-3 to prevent conflicts. Test simple prompts first. If responses are truncated, use `--summary` to condense. For bash scripts, use `--bash-best` or `--bash-error` to ensure robust, production-ready code. For performance-critical tasks, use `--bash-opt` to prioritize efficiency, and for multi-system compatibility, use `--bash-xplatform`.
- **Common Issues**: If a modifier fails due to platform limitations, GROK will default to standard output and suggest alternatives. For bash scripting, ensure scripts are tested in the target environment, as differences in shell versions, system utilities, or OS behaviors may cause issues. Use `--bash-env` or `--bash-deps` to address environment-specific or dependency-related challenges.
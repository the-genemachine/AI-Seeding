# Response Control Instructions

**Version: 1.1**  
**Last Updated: October 18, 2025**

Use these specific endings to control GROK's response format and length. These modifiers (also referred to as flags) allow users to tailor responses precisely. Modifiers are appended to the end of a prompt message.

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

### 18. Visual output (New)
   - End your message with `--chart` or `--visual`
   - GROK will generate or include visual elements such as charts, graphs, or images when applicable to enhance understanding

   Example:
   <prompt>
   "Show sales data trends --chart"
   </prompt>

### 19. Memory management (New)
   - End your message with `--reset-context`
   - GROK will reset the conversation context for a fresh start, or use `--handover` to generate a handover document summarizing key points for persistence across sessions

   Example:
   <prompt>
   "Summarize our project discussion --handover"
   </prompt>

### 20. Language selection (New)
   - End your message with `--lang=[language]` (e.g., `--lang=Spanish`)
   - GROK will provide the response in the specified language

   Example:
   <prompt>
   "Explain AI --lang=French"
   </prompt>

### 21. Priority emphasis (New)
   - End your message with `--accurate` or `--creative`
   - GROK will prioritize factual accuracy or creative elements in the response

   Example:
   <prompt>
   "Describe a future city --creative"
   </prompt>

## Additional Guidance

### Combining Modifiers
Multiple modifiers can be combined in a single prompt (e.g., `--short --formal`). GROK will apply them in the order provided, prioritizing non-conflicting aspects. If conflicts arise (e.g., `--short` and `--technical`), GROK will default to the first modifier and notify the user of the adjustment.

### Error Handling for Invalid or Misused Modifiers
If an unrecognized or invalid modifier is used (e.g., `--invalid`), GROK will respond with a brief error message indicating the issue and proceed with a standard response. For unsuitable applications (e.g., `--table` on non-tabular data), GROK will fall back to a list or paragraph format and explain the adaptation.

### Scope of Applicability
These modifiers are applicable across GROK's platforms, including grok.com, X apps, and API services. However, certain features like artifact creation may be limited in API mode due to output constraints.

### Expected Response Lengths
- Short modifiers (e.g., `--short`, `--Y/N`): 1-2 sentences or single word.
- Detailed modifiers (e.g., `--technical`, `--examples`): Typically 200-500 words, adjustable based on query complexity.
- Structured modifiers (e.g., `--list`, `--table`): Variable, focused on conciseness.

## Handover Document for Session Persistence
To maintain continuity across sessions, use the `--handover` modifier to request a handover document. This generates a structured summary of the conversation, including key decisions, code snippets, or unresolved items. The document can be downloaded or referenced in future sessions for seamless resumption.

Example:
<prompt>
"Generate a summary of our code discussion --handover"
</prompt>

GROK will produce a markdown-formatted handover file, which users can download and upload in subsequent interactions.

## Troubleshooting, Minimizing Hallucinations, and Maximizing Performance
- **Avoiding Hallucinations**: Use precise prompts with verifiable facts. Combine with `--verify` for fact-checking. If GROK detects potential inaccuracies, it will flag them.
- **Optimizing Prompts**: Be specific in instructions; avoid ambiguity. For complex queries, break them into steps using `--steps`.
- **Performance Tips**: Limit combined modifiers to 2-3 to prevent conflicts. Test simple prompts first. If responses are truncated, use `--summary` to condense.
- **Common Issues**: If a modifier fails due to platform limitations, GROK will default to standard output and suggest alternatives.
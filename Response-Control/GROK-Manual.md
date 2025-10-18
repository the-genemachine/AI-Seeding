# User Manual: Working with Response Control Flags

**Version: 1.0**  
**Last Updated: October 18, 2025**

This manual provides detailed instructions on utilizing the flags (modifiers) outlined in the Response Control Instructions document. It is designed as a standalone reference for effective application.

## Introduction
Flags are appended to the end of your prompt to dictate GROK's response style, format, or depth. They enhance control over outputs, ensuring responses align with user needs.

## Best Practices for Using Flags
1. **Placement**: Always place flags at the very end of your message, separated by spaces if combining multiple.
2. **Syntax**: Use double hyphens (--) followed by the flag name. Parenthetical alternatives (e.g., (short answer only)) are equivalent but less common.
3. **Combination Rules**: Up to three flags can be combined. Order matters for precedence (e.g., `--technical --short` prioritizes technical depth within a short format). Avoid contradictory pairs like `--technical --simple`.
4. **Testing**: Start with single flags to verify behavior before combining.
5. **Platform Considerations**: Flags work consistently across interfaces, but visual flags (e.g., `--chart`) may render differently in text-only environments.

## Flag Categories and Usage Tips
- **Length Control Flags** (--short, --Y/N, --summary): Ideal for quick answers. Use when brevity is essential.
- **Format Flags** (--list, --table, --steps): Structure complex information. Ensure your query lends itself to the format (e.g., comparisons for --table).
- **Depth and Tone Flags** (--technical, --simple, --formal, --casual): Adjust complexity or style. Pair with --examples for illustrative responses.
- **Content Enhancement Flags** (--examples, --code, --pros/cons, --compare): Add value through specifics. Use --code for programming queries.
- **Special Flags** (--artifact, --context, --verify, --chart, --lang, --accurate): For unique needs like visuals or verification. --handover is particularly useful for multi-session projects.
- **Memory Flags** (--reset-context, --handover): Manage conversation state. --handover creates a downloadable summary for persistence.

## Troubleshooting Flags
- If a flag does not apply, GROK will adapt and notify you.
- For errors, rephrase the prompt or remove conflicting flags.
- Maximize performance by aligning flags with query intent (e.g., avoid --visual on abstract topics).

This manual complements the main instructions document and can be referenced independently.
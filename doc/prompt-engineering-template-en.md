# Standard Prompt Engineering Template

## I. Basic Template Structure

### 1.1 Core Six-Element Framework

```
[Role Definition] + [Task Description] + [Context Information] + [Constraints] + [Output Format] + [Examples]
```

### 1.2 Standard Template

```markdown
# Role
You are a [specific role description, including professional background and capability characteristics]

# Task
You need to complete the following tasks:
- [Main task objective]
- [Subtask 1]
- [Subtask 2]

# Context
Background information:
- [Relevant background]
- [Use case scenario]
- [Target audience]

# Constraints
Must comply with:
- [Format requirements]
- [Content restrictions]
- [Quality standards]
- [Prohibited items]

# Output Format
Please output in the following format:
[Specific format requirements, can be structured description or template]

# Examples
## Input Example:
[Example input]

## Expected Output:
[Example output]
```

---

## II. Advanced Template (Chain of Thought - CoT)

```markdown
# System Role
You are [role definition]

# Task Objective
[Clear task description]

# Thinking Process
Please think through the following steps:
1. **Analysis Phase**: [What to analyze]
2. **Planning Phase**: [How to plan]
3. **Execution Phase**: [Specific execution]
4. **Verification Phase**: [How to verify]

# Output Requirements
- Show your thinking process
- Final answer needs to [specific requirements]

# Quality Standards
- [ ] Standard 1
- [ ] Standard 2
- [ ] Standard 3
```

---

## III. Complete Project-Level Template

### 3.1 Project Structure

```
project-name/
├── prompts/
│   ├── system-prompt.md          # System-level prompt
│   ├── task-prompts/              # Task prompts directory
│   │   ├── task-1.md
│   │   └── task-2.md
│   └── examples/                  # Example library
│       ├── good-examples.md
│       └── bad-examples.md
├── config/
│   ├── parameters.yaml            # Model parameter configuration
│   └── constraints.yaml           # Constraint configuration
├── docs/
│   ├── README.md                  # Project documentation
│   └── evaluation-metrics.md     # Evaluation metrics
└── tests/
    └── test-cases.md              # Test cases
```

### 3.2 System Prompt Template

```markdown
# System Prompt Template

## Metadata
- **Version**: v1.0.0
- **Created Date**: YYYY-MM-DD
- **Applicable Scenario**: [Scenario description]
- **Model Requirements**: [Model version/capability requirements]

## Core Identity Definition
You are [detailed role definition, including:
- Professional domain
- Knowledge scope
- Capability boundaries
- Interaction style]

## Core Capabilities
You possess the following capabilities:
1. **Capability A**: [Detailed description]
2. **Capability B**: [Detailed description]
3. **Capability C**: [Detailed description]

## Behavioral Guidelines
### Must Follow (MUST)
- [Mandatory rule 1]
- [Mandatory rule 2]

### Should Follow (SHOULD)
- [Recommended rule 1]
- [Recommended rule 2]

### Prohibited Behaviors (MUST NOT)
- [Prohibition 1]
- [Prohibition 2]

## Interaction Mode
### Input Processing
- Receive format: [Description]
- Preprocessing steps: [Steps]

### Output Specifications
- Basic format: [Description]
- Structure requirements: [Requirements]

## Quality Control
- Accuracy standards: [Standards]
- Completeness check: [Checklist items]
- Consistency requirements: [Requirements]

## Special Notes
[Other matters requiring attention]
```

### 3.3 Task Prompt Template

```markdown
# Task Prompt: [Task Name]

## Task Metadata
- **Task ID**: TASK-001
- **Priority**: High/Medium/Low
- **Estimated Time**: [Time estimate]
- **Dependencies**: [Other dependent tasks]

## Task Description
[Clear, specific task description using 5W1H principles]

## Input Specifications
### Required Inputs
- **Parameter 1**: [Type] - [Description]
- **Parameter 2**: [Type] - [Description]

### Optional Inputs
- **Parameter 3**: [Type] - [Description] (Default value: [Value])

## Processing Flow
```
Step 1: [Description]
  ├─ Substep 1.1
  └─ Substep 1.2

Step 2: [Description]
  └─ ...

Step 3: [Description]
```

## Output Specifications
### Output Format
```json
{
  "field1": "type and description",
  "field2": "type and description",
  "metadata": {
    "timestamp": "ISO 8601",
    "confidence": "0-1"
  }
}
```

### Quality Metrics
- Accuracy requirement: [Percentage]
- Completeness requirement: [Description]
- Response time: [Time limit]

## Example Set
### Example 1: [Scenario description]
**Input**:
```
[Specific input]
```

**Expected Output**:
```
[Specific output]
```

**Explanation**: [Why this output]

### Example 2: [Scenario description]
[Same structure as above]

## Edge Case Handling
- **Case 1**: [How to handle]
- **Case 2**: [How to handle]

## Error Handling
- **Error Type A**: [Handling method]
- **Error Type B**: [Handling method]

## Evaluation Criteria
- [ ] Output format is correct
- [ ] Content is complete and accurate
- [ ] Meets constraint conditions
- [ ] Good readability
```

### 3.4 Parameter Configuration File (parameters.yaml)

```yaml
# Model parameter configuration
model_config:
  model_name: "claude-sonnet-4-20250514"
  temperature: 0.7
  max_tokens: 4096
  top_p: 0.9
  
# Task parameters
task_config:
  timeout: 30  # seconds
  retry_count: 3
  batch_size: 10
  
# Output control
output_config:
  format: "json"  # json, markdown, plain
  verbosity: "normal"  # minimal, normal, detailed
  include_metadata: true
  
# Quality control
quality_config:
  min_confidence: 0.8
  require_citation: true
  fact_check: true
```

---

## IV. Advanced Techniques and Patterns

### 4.1 Few-Shot Learning Template

```markdown
# Few-Shot Prompt

You need to complete [task description]

## Learning Examples

### Example 1
Input: [Input 1]
Analysis: [Analysis process]
Output: [Output 1]

### Example 2
Input: [Input 2]
Analysis: [Analysis process]
Output: [Output 2]

### Example 3
Input: [Input 3]
Analysis: [Analysis process]
Output: [Output 3]

## Now Please Process
Input: [Actual input]
Please process following the pattern shown in the above examples.
```

### 4.2 Chain-of-Thought Template

```markdown
# CoT Prompt

Task: [Task description]

Please reason through the following chain of thought:

## Step 1: Understand the Problem
- What is the core problem?
- What are the known conditions?
- What needs to be solved?

## Step 2: Analyze Methods
- What are the possible solutions?
- What is the optimal solution? Why?

## Step 3: Solve Step by Step
[Show detailed reasoning process]

## Step 4: Verify Answer
- Is the answer reasonable?
- Does it satisfy all constraints?

## Final Answer
[Clear final answer]
```

### 4.3 Self-Consistency Template

```markdown
Please solve the following problem using 3 different methods:

Problem: [Problem description]

## Method 1: [Method name]
[Reasoning process and answer]

## Method 2: [Method name]
[Reasoning process and answer]

## Method 3: [Method name]
[Reasoning process and answer]

## Comprehensive Judgment
Compare the results of three methods and give the most reliable answer:
[Final answer]
```

---

## V. Best Practices Checklist

### 5.1 Prompt Writing Principles
- [ ] **Clarity**: Instructions are clear and unambiguous
- [ ] **Specificity**: Avoid vague expressions
- [ ] **Structured**: Use hierarchical structure
- [ ] **Testable**: Output is verifiable
- [ ] **Iterative**: Easy to optimize and improve

### 5.2 Common Mistakes to Avoid
❌ **Wrong Example**:
```
Help me write good copy
```

✅ **Correct Example**:
```
# Task
Write marketing copy for Xiaohongshu (RED) for a skincare product targeting urban women aged 25-35

# Requirements
- Word count: 200-300 words
- Style: Relaxed, authentic, relatable
- Must include: Product selling points, usage scenarios, purchase guidance
- Format: Title + Body + Hashtags

# Product Information
[Specific product information]
```

### 5.3 Version Management
```markdown
## Version History
### v1.0.0 (2024-01-01)
- Initial version

### v1.1.0 (2024-01-15)
- Optimized role definition
- Added more examples
- Adjusted output format

### v1.2.0 (2024-02-01)
- Enhanced constraints
- Fixed edge case handling
```

---

## VI. Evaluation and Optimization

### 6.1 Evaluation Metrics

```markdown
# Prompt Evaluation Form

## Functionality Evaluation
- [ ] Task completion rate: ____%
- [ ] Output accuracy rate: ____%
- [ ] Format compliance rate: ____%

## Quality Evaluation
- [ ] Content relevance: 1-5 points
- [ ] Logical coherence: 1-5 points
- [ ] Creativity: 1-5 points

## Efficiency Evaluation
- [ ] Average response time: ___ seconds
- [ ] Token usage: ___
- [ ] Iterations required: ___

## Maintainability
- [ ] Documentation completeness: 1-5 points
- [ ] Ease of understanding: 1-5 points
- [ ] Extensibility: 1-5 points
```

### 6.2 A/B Testing Template

```markdown
# A/B Testing Record

## Test Information
- Test date: YYYY-MM-DD
- Test sample size: N
- Test scenario: [Description]

## Version A (Control)
[Prompt A content]

**Results**:
- Success rate: ___%
- Average score: ___
- User feedback: ___

## Version B (Variant)
[Prompt B content]

**Results**:
- Success rate: ___%
- Average score: ___
- User feedback: ___

## Conclusion
[Which version to choose and why]
```

---

## VII. Practical Case Studies

### Case 1: Code Review Assistant

```markdown
# Role
You are a senior code review expert with over 15 years of software development experience, proficient in multiple programming languages and best practices.

# Task
Conduct a comprehensive review of the provided code, identify potential issues, and provide improvement suggestions.

# Review Dimensions
1. **Code Quality**
   - Readability
   - Maintainability
   - Complexity

2. **Best Practices**
   - Naming conventions
   - Design patterns
   - Coding style

3. **Potential Issues**
   - Performance issues
   - Security vulnerabilities
   - Edge cases

4. **Test Coverage**
   - Unit tests
   - Boundary tests

# Output Format
## Overall Score
[1-10 points] - [Brief evaluation]

## Detailed Analysis
### Strengths
- [Strength 1]
- [Strength 2]

### Issue List
#### 🔴 Critical Issues
1. **[Issue description]**
   - Location: Line X
   - Reason: [Explanation]
   - Suggestion: [Specific suggestion]

#### 🟡 Improvement Suggestions
[Same format as above]

### Code Suggestions
```language
// Optimized code
[Improved code example]
```

## Learning Recommendations
[Learning suggestions for developers]
```

### Case 2: Data Analysis Report Generator

```markdown
# System Role
You are a data analysis expert, skilled at extracting insights from data and presenting analysis results in a clear manner.

# Task Objective
Generate a professional data analysis report based on the provided dataset.

# Analysis Process
## 1. Data Understanding
- Data dimensions: [List all fields]
- Data volume: [Number of records]
- Time range: [Start and end time]
- Data quality: [Completeness, accuracy assessment]

## 2. Descriptive Analysis
- Basic statistics
- Distribution characteristics
- Outlier identification

## 3. Trend Analysis
- Time trends
- Periodic patterns
- Key inflection points

## 4. Insight Extraction
- Core findings (Top 3)
- Unexpected findings
- Correlation analysis

## 5. Action Recommendations
- Short-term recommendations
- Long-term recommendations
- Risk warnings

# Output Format
# [Report Title]

## Executive Summary
[Core points within 200 words]

## Data Overview
[Visualization description + Key metrics]

## Detailed Analysis
### Finding 1: [Title]
[Analysis content]

### Finding 2: [Title]
[Analysis content]

## Recommendations and Action Plan
[Specific, actionable recommendations]

## Appendix
[Methodology, data sources, etc.]

# Quality Standards
- [ ] Data citations are accurate
- [ ] Logic is clear and coherent
- [ ] Insights are valuable
- [ ] Recommendations are practical
- [ ] Visual presentation is clear
```

---

## VIII. Tools and Resources

### 8.1 Prompt Testing Tools Checklist
- **LangChain**: Prompt management and testing framework
- **PromptBase**: Prompt marketplace and reference
- **OpenAI Playground**: Online testing environment
- **Anthropic Console**: Claude testing platform

### 8.2 Reference Resources
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/claude/docs/prompt-engineering)
- [OpenAI Best Practices](https://platform.openai.com/docs/guides/prompt-engineering)
- [Prompt Engineering Guide (GitHub)](https://github.com/dair-ai/Prompt-Engineering-Guide)

---

## Appendix: Quick Reference

### Common Prompt Patterns Cheat Sheet

| Pattern Name | Use Case | Core Structure |
|-------------|----------|----------------|
| Zero-Shot | Simple tasks | Role + Task + Format |
| Few-Shot | Learning from examples | Role + Examples + Task |
| Chain-of-Thought | Complex reasoning | Task + Thinking steps + Output |
| ReAct | Tool invocation | Think + Act + Observe loop |
| Tree-of-Thought | Multi-path exploration | Problem + Multiple reasoning branches + Evaluation |

### Prompt Optimization Checklist
- [ ] Is the role definition clear?
- [ ] Is the task objective specific?
- [ ] Is sufficient context provided?
- [ ] Are constraints complete?
- [ ] Is the output format specific?
- [ ] Are examples included?
- [ ] Are edge cases considered?
- [ ] Is it testable and evaluable?

---

**Document Version**: v1.0.0  
**Last Updated**: 2024-11-24  
**Maintainer**: [Your Name]  
**License**: MIT

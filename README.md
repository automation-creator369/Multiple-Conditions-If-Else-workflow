# Multiple-Conditions-If-Else-workflow
this workflow admire multiple conditions in if else that categorized into high, medium, low with the help of gemini module
# AI-Powered Lead Qualification Automation

An AI-powered lead qualification workflow built using **Make.com, Gemini AI, Google Sheets, and Gmail**.

This project automates the process of analyzing incoming leads, classifying them based on budget and deadline, storing qualification results, and routing leads through different email paths using conditional logic.

## 🎯 Project Objective

The objective was to create an automated lead qualification system that reduces manual lead review and helps prioritize potential customers based on predefined business criteria.

Instead of manually reviewing every lead, the workflow uses Gemini AI to analyze lead information and Make.com to handle validation, data processing, conditional routing, and email automation.

## ⚙️ Workflow Architecture

**Google Sheets → Gemini AI → JSON Parser → Google Sheets → Filters → If-Else Logic → Gmail**

### 1. Lead Collection
Google Sheets acts as the source of incoming lead information, including budget and deadline.

### 2. AI-Based Lead Qualification
Gemini AI evaluates each lead using predefined qualification rules.

The AI classifies leads into five categories:

- High
- Medium
- Low
- Unqualified
- Invalid

### 3. Structured AI Output
Gemini generates structured JSON containing the lead's budget, deadline, category, and qualification reason.

The JSON Parser converts the AI response into structured fields that can be mapped throughout the workflow.

### 4. Qualification Results Storage
The qualification results are stored in Google Sheets for tracking and reviewing lead information.

### 5. Filtering and Conditional Routing
Before reaching the email automation stage, filters identify Unqualified and Invalid leads and prevent them from entering the Gmail paths.

The remaining leads proceed to the If-Else logic, which evaluates their final qualification category.

### 6. Multiple Gmail Paths
The workflow routes leads according to their category:

- **High:** Dedicated email response for high-priority leads.
- **Medium:** Separate email response for medium-priority leads.
- **Low:** Different email response for low-priority leads.

This allows each category to receive an appropriate response rather than sending the same email to every lead.

## 🛠️ Technologies Used

- Make.com — Workflow automation and conditional routing
- Gemini AI — AI-based lead analysis and classification
- Google Sheets — Lead collection and qualification results
- JSON — Structured AI output
- Gmail — Automated category-based email responses

## 🧠 Key Concepts Practiced

- AI integration into automation workflows
- Prompt engineering and structured JSON generation
- Data mapping between Make modules
- Validation and filtering
- Multiple-condition logic
- Conditional branching and routing
- Bundle processing and execution limits
- Debugging workflow behavior
- Designing category-specific email automation

## 🔍 Challenges and Learnings

One challenge involved understanding why Gemini processed multiple leads during a single scenario execution.

After investigating the workflow, I identified the Google Sheets Watch New Rows module's **Limit** setting as the cause.

This helped me understand how Make handles bundles, operations, and data flow through downstream modules.

The project reinforced an important lesson: successful automation requires more than connecting modules. It requires understanding how data moves, how conditions are evaluated, and how unexpected behavior can be diagnosed.

## 📌 Project Status

Completed as a practical learning project.

The workflow demonstrates how AI-based classification can be combined with structured data and conditional logic to automate lead qualification and email responses.

## 👨‍💻 Author

A BCA student learning AI automation, workflow design, and practical problem-solving through hands-on projects.

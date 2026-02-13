---

## 7. ADVANCED TECHNIQUES (The "Power User" Suite)
*For complex problems, higher accuracy, and automated workflows.*

### A. Self-Consistency (The "Majority Vote")
**Best for:** Ensuring accuracy in math, logic, or fact-based questions.
**How it works:** Instead of asking the AI once, you ask it to generate the answer multiple times (or reason through it in different ways) and pick the most consistent answer.
> **Template:**
> "Solve the following problem. Generate 3 different distinct reasoning paths to find the answer. If the answers differ, select the one that appears most frequently.
> **Problem:** [Insert Math/Logic Problem]"

### B. Generated Knowledge Prompting
**Best for:** Questions requiring specific common sense or niche knowledge that the AI might hallucinate.
**How it works:** You ask the AI to first list "facts" about the topic, then use those facts to answer the question.
> **Template:**
> "Step 1: Generate 5 key facts about [Topic, e.g., 'The Rules of Golf'].
> Step 2: Using those facts, answer this question: [Insert Question, e.g., 'Can you win with a higher score?']"

### C. Prompt Chaining
**Best for:** massive tasks that confuse the AI if asked all at once (e.g., writing a whole book or analyzing a 50-page report).
**How it works:** Break the task into sub-prompts. The output of Prompt 1 becomes the input for Prompt 2.
> **Workflow Example:**
> * **Prompt 1:** "Extract the key quotes from this document." -> [Copy Output]
> * **Prompt 2:** "Use these quotes to write a summary." -> [Copy Output]
> * **Prompt 3:** "Format this summary into a client email."

### D. Tree of Thoughts (ToT)
**Best for:** Complex problem solving, brainstorming, or strategy.
**How it works:** Ask the AI to simulate multiple "experts" proposing different solutions, critiquing each other, and converging on the best one.
> **Template:**
> "Imagine three different experts are answering this question.
> All experts will write down 1 step of their thinking, then share it with the group.
> If any expert realizes they are wrong, they leave.
> **The Question:** [Insert complex strategic question]"

### E. Retrieval Augmented Generation (RAG)
*Note: This usually requires a technical setup, but the concept is vital.*
**Best for:** Answering questions using *your* private company data (PDFs, Databases) that the AI doesn't know.
**Concept:** Instead of just asking ChatGPT, you first "retrieve" the relevant page from your company manual, paste it into the prompt, and say "Answer using only this context."

### F. ReAct (Reason + Act)
**Best for:** Agents that need to use tools (like a calculator or Google Search).
**How it works:** You force the AI to follow a strict loop: **Thought** (What do I need to do?) -> **Action** (Search Google) -> **Observation** (Read result) -> **Answer**.
> **Template:**
> "Question: What is the current stock price of Apple multiplied by 2?
> Use the following format:
> Thought: I need to find the stock price first.
> Action: Search [Apple stock price]
> Observation: [Paste search result]
> Thought: Now I need to multiply it by 2.
> Answer: [Final Result]"

---

## 8. AUTOMATION & OPTIMIZATION TECHNIQUES
*Methods used to make prompts write themselves or improve automatically.*

### G. Meta Prompting
**Best for:** Creating reusable templates for recurring tasks.
**How it works:** Instead of giving the AI specific examples (like in Few-Shot), you give it a "structural template" or abstract rules on *how* to solve a type of problem. You focus on the *syntax* and *form* rather than the content.
> **Template:**
> "I want you to act as a [Role].
> Whenever I give you a task, follow this abstract structure:
> 1. Analyze the input type.
> 2. Identify the core constraint.
> 3. Output the solution in JSON format.
> Do not deviate from this structure."

### H. Automatic Prompt Engineer (APE)
**Best for:** When you don't know the best way to ask.
**How it works:** You ask the AI to write the prompt for you.
> **Template:**
> "I need to get a highly accurate summary of medical texts.
> Generate 5 different prompt variations that would give me the best results.
> Evaluate which one is likely to be most effective and explain why."

### I. Reflexion (Self-Correction)
**Best for:** Coding, writing, or tasks where "getting it right the first time" is hard.
**How it works:** You ask the AI to critique its own work and then rewrite it.
> **Template:**
> "Step 1: Write a blog post about [Topic].
> Step 2: Review the blog post above. List 3 ways it could be more engaging and concise.
> Step 3: Rewrite the post implementing those improvements."

### J. Program-Aided Language Models (PAL)
**Best for:** Math or precise calculations where AIs often make mistakes.
**How it works:** Instead of asking the AI to *calculate* the answer, ask it to write a *code script* (like Python) that calculates the answer.
> **Template:**
> "Don't calculate this math problem textually.
> Instead, write a Python script that solves the problem.
> **Problem:** [Insert Math Problem]"

### K. Active-Prompt
**Best for:** Training the AI on specific, hard edge cases.
**How it works:** You identify questions where the AI is "uncertain" or inconsistent, and you specifically provide human-written examples for *those* hard cases to guide it.

### L. Multimodal Chain-of-Thought
**Best for:** Tasks involving images and text.
**How it works:** Just like standard Chain-of-Thought, but you ask the AI to reason about the *image* step-by-step before giving the final answer.
> **Template:**
> "[Upload Image]
> First, describe the key elements visible in this chart.
> Second, explain the trend shown.
> Finally, answer: What is the projected growth for 2025?"

---
*Added to Prompt Engineering Guide v1.1*

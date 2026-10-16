# MathPath AI — Web-Based AI Math Differentiator

A responsive educational web app prototype for the assignment **AI for Differentiated Learning**. It adapts a core math task across Foundation, Standard, and Advanced levels with tailored hints, feedback, and solutions.

## Run locally
Open `index.html` in a browser. No build step or dependencies are required.

## Deploy to GitHub Pages
1. Create a public GitHub repository (e.g. `mathpath-ai-differentiator`).
2. Upload `index.html` and this `README.md`.
3. In repository Settings → Pages, deploy from the `main` branch and `/ (root)`.
4. Wait for GitHub Pages to publish and copy the live URL for submission.

## Current functionality
- Responsive layout
- Difficulty toggle: Foundation / Standard / Advanced
- Topic toggle: linear equations / factoring expressions
- Adapted tasks, progressive hints, answer checking, and step-by-step solutions
- Works offline in demo mode

## Important AI integration note
This prototype uses prepared examples in the browser so it runs immediately without a secret key. The assignment asks for a live AI model API. To complete that requirement, connect the front end to a backend endpoint (e.g. Flask) that calls an LLM using a server-side environment variable such as `OPENAI_API_KEY`. **Never put a private API key in browser JavaScript or commit it to GitHub.** A production AI version should validate the model's math and use structured JSON output.

## Suggested prompt for the backend
"You are a mathematics teacher designing differentiated practice. Topic: {topic}. Learner stage: {grade}. Level: {level}. Learner difficulty: {difficulty}. Return valid JSON with: problem, context, three hints ordered from subtle to explicit, answer, and solution_steps. Foundation: simple numbers, direct scaffolding and step-by-step support. Standard: grade-level independent problem solving. Advanced: multi-step reasoning or a realistic application. Ensure the answer and every step are mathematically correct. Do not include extra keys."

## Files
- `index.html` — complete front-end prototype
- `report.md` — one-page report draft

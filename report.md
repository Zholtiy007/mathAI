# Brief Report: MathPath AI — AI for Differentiated Learning

## Purpose
MathPath AI is a web-based mathematics differentiator. It takes one core mathematical concept—solving linear equations—and adapts the practice task, scaffolding, and feedback for learners at three levels. A second topic, factoring expressions, is included to demonstrate that the approach can be reused.

## Differentiation design
- **Level 1 — Foundation:** simple equations, direct hints, and short, explicit solution steps. The aim is to reduce cognitive load while helping a learner understand inverse operations.
- **Level 2 — Standard:** curriculum-level equations that require multiple operations, collecting like terms, or using the distributive property. Hints support independent problem solving without giving away every step.
- **Level 3 — Advanced:** multi-step equations and an applied word problem. Learners are prompted to model a situation, combine operations, and verify their answers.

The interface allows a learner to select a topic, level, and grade band. Hints are revealed progressively, answers receive immediate feedback, and a full worked solution is available when needed. This makes the amount of support responsive to the selected learner level.

## Prompt design for the AI component
The proposed backend prompt is:

> You are a mathematics teacher designing differentiated practice. Topic: {topic}. Learner stage: {grade}. Level: {level}. Learner difficulty: {difficulty}. Return valid JSON with: problem, context, three hints ordered from subtle to explicit, answer, and solution_steps. Foundation: simple numbers, direct scaffolding and step-by-step support. Standard: grade-level independent problem solving. Advanced: multi-step reasoning or a realistic application. Ensure the answer and every step are mathematically correct. Do not include extra keys.

The prompt explicitly conditions the task on the topic, learner stage, selected level, and learner-reported difficulty. It requests a predictable output structure so the website can display the problem, hints, answer, and solution separately.

## AI implementation and validation
The included front end currently runs in **demo mode** with prepared examples, so it can be tested and deployed without an API key. To fully meet the AI-integration requirement, the next implementation step is a small backend endpoint that sends the prompt to an AI model using a server-side API key stored in an environment variable. The response should be parsed as JSON and checked for mathematical consistency before it is shown to students. This is important because AI-generated mathematics can contain errors.

## Conclusion
MathPath AI demonstrates differentiated learning through level-specific problem complexity and adaptive scaffolding. Its interface is ready as a working prototype; live model integration and deployment are required before it can be truthfully submitted as a fully AI-connected live website.

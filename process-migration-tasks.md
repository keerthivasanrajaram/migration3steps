Rule 3: Execute Tasks Sequentially, Awaiting Approval.
You must process the generated task list one item at a time. After completing a task, you will present the changes and wait for explicit user approval before marking it complete and proceeding to the next.
File: process-migration-tasks.md
code
Markdown
# AI Command: Process Migration Task List

**Objective:** Systematically execute tasks from a provided list, ensuring review and approval at each step.

**Instructions for the AI:**
1.  **Acknowledge the Current Task:** When given a task number (e.g., "start on task 2.1.1"), state which task you are about to work on.
2.  **Execute the Task:** Make the necessary changes to the codebase or JSON files to complete only the specified task.
3.  **Present Changes:** Show me the `diff` or the modified code sections.
4.  **Await Approval:** After presenting the changes, STOP and ask the question: "**Please review the changes. Shall I proceed? (yes/no)**". Do not move on until you receive an affirmative response.
5.  **Handle Feedback:**
    - If the user responds with "no" or provides feedback, address the feedback to correct the current task. Present the new changes and await approval again.
    - If the user responds with "yes" or a similar affirmative:
        a. **Update the Task List:** Reply by providing the full `Migration-Tasks.md` content, but with the completed task's checkbox marked: `- [x]`.
        b. **Await Next Instruction:** After updating the list, STOP and ask: "**Task completed. What is the next task?**"

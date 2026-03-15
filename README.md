# Claude Code Tutorial: Learn from Scratch

Welcome to your Claude Code learning project! This tutorial teaches you how Claude Code works and how to harness its power using the `.claude` folder. Whether you're new to AI-assisted development or looking to master Claude Code, start here!

### Watch The Full Tutorial On YOUTUBE
- https://youtu.be/lkc-F5I8gFE?si=MFLyX0RVkcHrM2nr

---

## What is Claude Code?

**Claude Code** is an intelligent coding assistant that helps you write, review, debug, and understand code. It learns from your project's rules and works the way *you* want it to work.

Think of it like having an expert developer as a pair programmer—but one that understands your project's unique style and requirements.

### Key Capabilities:
- 💬 **Ask questions** about your code
- 🐛 **Debug issues** with detailed explanations
- ✨ **Generate code** following your standards
- 📚 **Learn** best practices for your project
- 🤖 **Automate tasks** with custom skills and agents

---

## The `.claude` Folder: Your Command Center

The `.claude` folder is where you teach Claude Code about your project. It's like a configuration hub that tells Claude:
- **How to code** (your standards and style)
- **What it can do** (custom skills for tasks)
- **How to specialize** (different agents for different jobs)
- **What it remembers** (persistent memory across sessions)

---

## 📁 Folder Structure Overview

Here's what's inside `.claude` and what each part does:

```
.claude/
├── CLAUDE.md              # 📖 Your project's "rulebook"
├── skills/                # 🛠️ Custom tools for specific tasks
│   ├── fetchAPI/          # Fetch data from APIs
│   ├── migrate/           # Move data between locations
│   └── visualize/         # Create visualizations
├── agents/                # 🤖 Specialized Claude personalities
│   ├── code_reviewer/     # Expert code reviewer
│   └── orchestrator/      # Workflow coordinator
├── agent-memory/          # 🧠 What Claude remembers
├── hooks/                 # 🪝 Custom automation triggers
├── settings.json          # ⚙️ Global configuration
├── settings.local.json    # 💻 Local machine settings
└── scheduled_tasks.lock   # 🔒 Task scheduling file
```

---

## 📚 Core Components Explained

### 1️⃣ **CLAUDE.md** – Teaching Claude Your Standards

This file is like an instruction manual for Claude Code. It defines:

**What it covers:**
- 🎨 **Coding Style** – PEP 8 for Python, naming conventions
- 🏷️ **Type Annotations** – Using type hints for clarity
- 📝 **Documentation** – How to write good docstrings
- 📦 **Dependencies** – Managing libraries and versions
- 📂 **Project Organization** – How files should be structured
- 📋 **Best Practices** – Error handling, version control, etc.

**Why it matters:**
When you write code or ask Claude to write code, it reads this file and ensures everything follows your project's rules. It's like having a style guide that Claude automatically applies!

**Example:** If your CLAUDE.md says "use snake_case for functions," Claude will always suggest function names like `fetch_data()` instead of `fetchData()`.

---

### 2️⃣ **Skills** – Giving Claude Superpowers

Skills are specialized modules that teach Claude how to do specific tasks in your project. Instead of Claude giving generic answers, it can perform targeted operations.

#### **Skill #1: fetchAPI** 📡
- **Purpose:** Fetch data from external APIs
- **What it can do:** Connect to APIs, handle responses, store data
- **Location:** `.claude/skills/fetchAPI/`
- **Example use:** "Fetch weather data from OpenWeatherMap"

#### **Skill #2: migrate** 🚀
- **Purpose:** Move and transform data
- **What it can do:** Migrate data between locations, track operations
- **Location:** `.claude/skills/migrate/`
- **Example use:** "Move the fetched data to the database"

#### **Skill #3: visualize** 📊
- **Purpose:** Create visual representations
- **What it can do:** Generate charts, graphs, analytics dashboards
- **Location:** `.claude/skills/visualize/`
- **Example use:** "Create a chart showing today's sales"

**How Skills Work (Step-by-Step):**
1. You ask Claude to do something
2. Claude checks available skills
3. If a relevant skill exists, Claude uses it
4. The skill executes the task and returns results

**Learn by Example:**
Request: "Get weather data from an API and show me a chart"
1. Claude invokes `fetchAPI` skill → fetches weather data
2. Claude invokes `visualize` skill → creates a chart
3. Results saved automatically!

---

### 3️⃣ **Agents** – Claude's Specialized Personas

Agents are like different "versions" of Claude, each specialized for a specific job. Each agent has its own:
- Custom instructions and expertise
- Memory of past interactions
- Specific workflow optimizations

#### **Agent #1: code_reviewer** 👀
- **Specialization:** Reviews your code for quality, bugs, and improvements
- **Memory:** Remembers patterns and feedback from previous reviews
- **Location:** `.claude/agents/code_reviewer/`
- **When to use:** "Review this code" or "Check for issues"

#### **Agent #2: orchestrator** 🎼
- **Specialization:** Manages complex multi-step workflows
- **Memory:** Tracks task dependencies and execution order
- **Location:** `.claude/agents/orchestrator/`
- **When to use:** Complex projects with many interconnected tasks

**Agent Memory (The Smart Part!):**
- 🧠 Each agent learns from interactions
- 📝 Memories are saved in `.claude/agent-memory/`
- 🔄 Information persists across sessions
- 📈 Improves quality over time as agent learns your preferences

---

### 4️⃣ **Settings** – Fine-Tuning Claude's Behavior

Two configuration files control how Claude Code behaves:

**settings.json** (Team Configuration)
- Global settings for everyone working on the project
- Check this into version control
- Example: "Always use Python 3.10+"

**settings.local.json** (Personal Preferences)
- Your local machine preferences
- Don't share with the team
- Example: Your preferred IDE theme or notification settings

---

## 🔄 How It All Works Together

Here's the flow when you use Claude Code in this project:

```
You ask Claude to do something
        ↓
Claude reads CLAUDE.md (your standards)
        ↓
Claude checks available skills
        ↓
Claude selects the right agent
        ↓
Claude applies your standards + uses relevant skills
        ↓
Claude saves to agent-memory for next time
        ↓
You get smarter, contextual results!
```

**Real Example Walkthrough:**

**You:** "Review my new Python function for bugs and style issues"

**Claude Code does this:**
1. ✅ Reads CLAUDE.md → learns your PEP 8 style rules
2. ✅ Loads code_reviewer agent → uses its expertise
3. ✅ Reviews function against standards
4. ✅ Saves feedback to agent memory → improves next time
5. ✅ Returns detailed review with fixes

---

## 🎓 Tutorial: Learning Path

### Beginner Level
Choose one of these to start:

**Challenge 1: Understand CLAUDE.md**
- Open [`.claude/CLAUDE.md`](.claude/CLAUDE.md)
- Read the project standards
- Ask Claude: "Explain the coding standards in this project"

**Challenge 2: Explore Skills**
- Look at `.claude/skills/` folder
- Pick one skill (like `fetchAPI`)
- Read its `SKILL.md` file
- Ask Claude: "What can the fetchAPI skill do?"

**Challenge 3: Meet the Agents**
- Check `.claude/agents/`
- Look at `code_reviewer` configuration
- Ask Claude: "Review this code for me"

### Intermediate Level

**Challenge 4: Request Automated Tasks**
- Ask Claude: "Fetch data from [API] and create a visualization"
- Claude will use both `fetchAPI` and `visualize` skills
- Understand how skills work together

**Challenge 5: Agent Integration**
- Say: "I'm working on a complex feature—help me orchestrate the workflow"
- Claude uses the orchestrator agent
- Observe how specialized agents differ from standard Claude

**Challenge 6: Create Your First Custom Skill**
- Design a new task you want to automate
- Create a folder in `.claude/skills/`
- Write a `SKILL.md` file with instructions
- Ask Claude to use it!

### Advanced Level

**Challenge 7: Train Agent Memory**
- Have multiple conversations asking Claude the same type of question
- Notice how responses improve over time
- Check `.claude/agent-memory/` to see what Claude learned

**Challenge 8: Customize Settings**
- Edit `.claude/settings.json` and `.claude/settings.local.json`
- Experiment with different configurations
- Observe how Claude behavior changes

**Challenge 9: Create a New Agent**
- Define a specialized agent for your workflow
- Create a new folder in `.claude/agents/`
- Configure its unique instructions
- Use it for specialized tasks

---

## 💡 Quick Examples

### Example 1: The Standard Developer
```
Scenario: You keep asking Claude to fix code, but the formatting is wrong

Solution: Claude reads CLAUDE.md and now automatically:
✓ Uses PEP 8 formatting
✓ Adds type annotations
✓ Includes docstrings
✓ Follows naming conventions
```

### Example 2: The Automated Workflow
```
Scenario: "Fetch user data from API, migrate to database, show me a report"

What happens:
1. fetchAPI skill → gets the data
2. migrate skill → moves it to database
3. visualize skill → creates a report
All following your project's standards!
```

### Example 3: The Smart Reviewer
```
Scenario: First code review vs. 5th code review by code_reviewer agent

First time: Generic feedback
Fifth time: Specific to YOUR patterns and preferences
Why? Agent memory learned what matters to you!
```

---

## 🎯 What You'll Learn

By exploring this project, you'll understand:

✅ **What is Claude Code** – An AI assistant for developers
✅ **The `.claude` folder** – Control center for customization  
✅ **CLAUDE.md** – Teaching Claude your standards
✅ **Skills** – Automating specific tasks
✅ **Agents** – Creating specialized versions of Claude
✅ **Memory** – How Claude learns and improves
✅ **Settings** – Fine-tuning behavior
✅ **Real workflows** – Putting it all together

---

## 🚀 Next Steps

### Ready to Dive In?

1. **Start Small:** Read [`.claude/CLAUDE.md`](.claude/CLAUDE.md) (5 min)
2. **Explore:** Browse the `.claude/skills/` folder (5 min)
3. **Ask Claude:** Open VS Code and ask Claude questions about this project
4. **Experiment:** Try one of the beginner challenges above
5. **Build:** Create your own skill or agent!

### Recommended Reading Order:
1. This README (you're reading it! ✓)
2. [`.claude/CLAUDE.md`](.claude/CLAUDE.md) – Project standards
3. `.claude/skills/fetchAPI/SKILL.md` – Your first skill
4. `.claude/agents/code_reviewer/code_reviewer.md` – Your first agent
5. Experiment with Claude Code in VS Code

### Common Questions:

**Q: How do I use Claude Code?**
A: Open any file, press Ctrl+I (or Cmd+I on Mac), and start asking questions!

**Q: Can I change CLAUDE.md?**
A: Yes! Edit it to reflect your actual project standards and Claude will follow them.

**Q: How do I create my own skill?**
A: Create a folder in `.claude/skills/`, add a `SKILL.md` file with instructions, and Claude will recognize it.

**Q: Does Claude really remember things?**
A: Yes! Check `.claude/agent-memory/` to see what Claude learns across conversations.

---

## 📖 External Resources

- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [Claude Code Setup Guide](https://github.com/features/copilot)
- [PEP 8 – Python Style Guide](https://peps.python.org/pep-0008/)
- [PEP 257 – Docstring Conventions](https://peps.python.org/pep-0257/)

---

## 🎓 Project Goals

This tutorial project demonstrates:
- How to structure `.claude` folder for education
- Best practices for teaching Claude Code
- Real-world skill and agent examples
- Practical learning path for beginners

**Built with the goal:** Help you master Claude Code from scratch! 🚀

---

**Happy learning! Now open VS Code and start exploring Claude Code! 💻**

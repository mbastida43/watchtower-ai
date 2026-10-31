# Skills

how to add them:

# Adding Skills in Claude Code

To add a skill in Claude Code, you can install it globally, add it to a specific project, or sync it from your Claude account.

## Method 1: Add a Skill to a Specific Project (Team / Local)
You can place a skill folder directly inside your project directory so anyone working on the repository can use it:
1. Create the skill folder inside your project root:
   ```bash
   mkdir -p .claude/skills/<skill-name>
   ```
2. Place your `SKILL.md` file (and any supporting reference files) inside `.claude/skills/<skill-name>/`.
3. Commit the folder to your repository to share it with your team:
   ```bash
   git add .claude/skills
   git commit -m "Add custom skill"
   ```
4. Restart your Claude Code session and run `/skills` to verify.

## Method 2: Add a Personal Skill Globally
To make a skill available across all your projects on your machine, place it in your global user skills directory:
1. Put your skill folder and `SKILL.md` into `~/.claude/skills/<skill-name>/`.
2. Start or restart a Claude Code session.

## Method 3: Sync Skills from Claude.ai
If you created or enabled a skill in your web or desktop Claude account, it will automatically sync to Claude Code:
* Sign in to Claude Code using the same account you use on claude.ai (requires Claude Code v2.1.273 or later).
* Run `/skills` in the terminal to view your synced skills listed under `claude.ai sync`.
* *(Note: Skills do not sync if you are logged in via an API key or running inside a cloud provider like Amazon Bedrock).*

## Method 4: Install via Plugin Marketplace
1. Start a Claude Code session.
2. Type `/plugin` and press Enter to open the plugin browser.
3. Navigate to the **Discover** tab and select the skill/plugin you want to install.

# Skill Name

<!-- A concise, one-sentence description of what this skill does -->
A brief overview of the skill's purpose and utility.

# Skill Template

## Prerequisites

<!-- List any dependencies, keys, or tools required to run this skill -->
* Python 3.10+ (if running custom scripts)
* Environment variables: `MY_API_KEY` (if applicable)
* Required CLI tools installed globally

## Configuration

<!-- How to set up or configure the skill within the environment -->
To configure this skill, ensure the following configuration options or files are present:

```json
{
  "setting_name": "value"
}
```

## Usage

<!-- Explain the syntax, commands, or natural language prompts used to trigger this skill -->
To trigger this skill during a Claude Code session, you can use the following commands or prompt structures:

### Command Line / Slash Commands
```bash
/skill-command [arguments]
```

### Natural Language Examples
* "Analyze the current project using [Skill Name]."
* "Run the automation workflow for the latest commit."

## Examples

### Example 1: Basic Execution
**Input Prompt:**
> "Run the skill on the main branch."

**Expected Output:**
```text
[Skill] Starting execution...
[Skill] Processing completed successfully.
```

### Example 2: Advanced Usage
Describe a more complex scenario involving optional flags, parameters, or edge cases here.

## Troubleshooting

* **Issue:** Skill not recognized by Claude Code.  
  **Solution:** Run `/skills` to verify installation. Restart the session if necessary.
* **Issue:** Permission denied errors.  
  **Solution:** Ensure the underlying scripts or binaries have execution permissions (`chmod +x <file>`).

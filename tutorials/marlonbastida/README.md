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


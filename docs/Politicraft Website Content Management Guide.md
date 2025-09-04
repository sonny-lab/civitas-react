# Politicraft Website Content Management Guide

## Overview

Your Politicraft website now uses Markdown files for content management, making it much easier to add and update blog posts and development updates without editing JavaScript code.

## Content Structure

```
politicraft-website/
├── content/
│   ├── blog/           # Blog posts go here
│   └── development/    # Development updates go here
├── update_content.sh   # Script to build and prepare updates
└── ...
```

## Adding New Blog Posts

1. **Create a new file** in `/home/ubuntu/politicraft-website/content/blog/`
2. **Name it descriptively** with `.md` extension (e.g., `new-feature-announcement.md`)
3. **Use this format:**

```markdown
---
title: "Your Blog Post Title"
date: "Month Year"
excerpt: "A brief description that appears in the blog list."
---

# Your Blog Post Title

Write your content here using Markdown formatting.

## You can use headings

- Bullet points
- Lists
- **Bold text**
- *Italic text*
- [Links](https://example.com)

And regular paragraphs of text.
```

## Adding Development Updates

1. **Create a new file** in `/home/ubuntu/politicraft-website/content/development/`
2. **Name it descriptively** with `.md` extension (e.g., `multiplayer-system.md`)
3. **Use this format:**

```markdown
---
title: "Development Update Title"
status: "In Progress"
description: "Brief description of what this update covers."
---

# Development Update Title

Detailed content about the development progress.

## Current Status
- ✅ Completed tasks
- 🔄 In progress tasks  
- ⏳ Planned tasks

## Next Steps
What's coming next...
```

**Status Options:**
- `"In Progress"` - Currently being worked on
- `"Planning"` - In planning/design phase
- `"Completed"` - Finished
- `"Research Phase"` - Research and investigation

## Publishing Updates

After adding or editing content:

1. **Run the update script:**
   ```bash
   /home/ubuntu/politicraft-website/update_content.sh
   ```

2. **Notify the agent** to package and publish the website

3. **Click "Publish"** when the button appears in your UI

4. **Check your live site** at https://politicraft-mcnzj9.manus.space/

## Markdown Formatting Tips

### Headings
```markdown
# Main Heading
## Sub Heading
### Smaller Heading
```

### Text Formatting
```markdown
**Bold text**
*Italic text*
`Code text`
```

### Lists
```markdown
- Bullet point 1
- Bullet point 2

1. Numbered item 1
2. Numbered item 2
```

### Links
```markdown
[Link text](https://example.com)
```

### Images
```markdown
![Alt text](image-url)
```

## File Naming Best Practices

- Use lowercase letters
- Replace spaces with hyphens
- Be descriptive but concise
- Examples:
  - `welcome-to-politicraft.md`
  - `gameplay-mechanics-update.md`
  - `user-interface-progress.md`

## Content Organization Tips

### Blog Posts
- Sort by date (newest first automatically)
- Use clear, engaging titles
- Write compelling excerpts
- Keep posts focused on one main topic

### Development Updates
- Use consistent status labels
- Include specific progress details
- Mention timelines when possible
- Update existing files rather than creating duplicates

## Troubleshooting

If the build fails:
1. Check your Markdown syntax
2. Ensure the frontmatter (content between `---`) is properly formatted
3. Make sure file names don't have spaces or special characters
4. Verify all required fields are present in the frontmatter

## Quick Reference Commands

```bash
# Navigate to content directories
cd /home/ubuntu/politicraft-website/content/blog/
cd /home/ubuntu/politicraft-website/content/development/

# Create a new blog post
touch /home/ubuntu/politicraft-website/content/blog/my-new-post.md

# Create a new development update  
touch /home/ubuntu/politicraft-website/content/development/my-update.md

# Build and prepare for publishing
/home/ubuntu/politicraft-website/update_content.sh
```

This system allows you to focus on writing content without worrying about breaking the website code!


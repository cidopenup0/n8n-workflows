# Viral Tweet Scheduler – n8n Workflow

This workflow automatically generates and posts tweets to X (Twitter) using an LLM. It posts every 6 hours at a random minute so the schedule appears natural. You can also run it manually whenever needed.

## What the workflow does
1. Schedules posting every 6 hours with a randomized minute.
2. Generates a tweet using your niche, style, and inspiration settings.
3. Validates that the tweet fits within 280 characters.
4. Posts the tweet automatically.
5. Allows manual posting on demand.

## Main components
- Sticky Notes: Describe each workflow step.
- Schedule Trigger: Starts the workflow every 6 hours.
- Set Node: Stores influencer profile details.
- LLM Chain: Generates a tweet.
- IF Node: Checks tweet length.
- Twitter Node: Posts the tweet.
- Manual Trigger: Triggers posting manually.

## Customization
### Edit influencer profile
Modify the “Configure your influencer profile” node values:
- niche
- style
- inspiration

### Change posting frequency
Adjust the “Schedule posting every 6 hours” node:
- Change hoursInterval

### Change AI model
Modify the model name in the OpenRouter Chat Model node.

### Adjust tweet style
Edit the instructions in the Basic LLM Chain node.

### Remove or modify hashtags/emojis
Update the final instruction in the LLM prompt.


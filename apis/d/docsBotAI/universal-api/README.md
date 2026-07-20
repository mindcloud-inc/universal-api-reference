# <img src="https://images.mindcloud.co/apps/icons/docs-bot-ai_1774559043234.png" alt="DocsBot AI logo" width="28" height="28"> DocsBot AI: Universal API

Build and manage DocsBot teams, bots, sources, webhooks, leads, research jobs, and analytics through the DocsBot Admin API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docsBotAI/latest
- **Category:** Support / Ticketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docsbot.ai
- **Vendor API docs:** https://docsbot.ai/documentation/developer

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | POST | Creates a new bot in DocsBot AI. |
| [Delete Bot](actions/delete-bot.md) | DELETE | Deletes an existing bot from DocsBot AI. |
| [Get Bot](actions/get-bot.md) | GET | Retrieves a bot from DocsBot AI. |
| [List Bots](actions/list-bots.md) | GET | Retrieves bots from DocsBot AI. |
| [Update Bot](actions/update-bot.md) | PUT | Updates an existing bot in DocsBot AI. |

### Bot Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Bot Reports](actions/get-bot-reports.md) | GET | Retrieves bot reports from DocsBot AI. |

### Bot Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Bot Statistics](actions/get-bot-statistics.md) | GET | Retrieves bot statistics from DocsBot AI. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Delete Conversation](actions/delete-conversation.md) | DELETE | Deletes an existing conversation from DocsBot AI. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from DocsBot AI. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from DocsBot AI. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes an existing lead from DocsBot AI. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from DocsBot AI. |

### Lead Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Leads CSV](actions/export-leads-csv.md) | GET | Retrieves a leads CSV export from DocsBot AI. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Delete Question](actions/delete-question.md) | DELETE | Deletes a question from DocsBot AI. |
| [List Questions](actions/list-questions.md) | GET | Retrieves questions from DocsBot AI. |

### Research Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Research Job](actions/get-research-job.md) | GET | Retrieves a research job from DocsBot AI. |
| [List Research Jobs](actions/list-research-jobs.md) | GET | Retrieves research jobs from DocsBot AI. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Source](actions/create-source.md) | POST | Creates a new source in DocsBot AI. |
| [Delete Source](actions/delete-source.md) | DELETE | Deletes an existing source from DocsBot AI. |
| [Get Source](actions/get-source.md) | GET | Retrieves a source from DocsBot AI. |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources from DocsBot AI. |
| [Retry Source Indexing](actions/retry-source-indexing.md) | PUT | Updates a source to retry indexing in DocsBot AI. |

### Source Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create Presigned Upload URL](actions/create-presigned-upload-url.md) | GET | Retrieves a presigned upload URL from DocsBot AI. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from DocsBot AI. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from DocsBot AI. |
| [Update Team](actions/update-team.md) | PUT | Updates an existing team in DocsBot AI. |

### Team Invite

| Action | Method | Description |
| --- | --- | --- |
| [Invite Team Member](actions/invite-team-member.md) | POST | Creates a team invite in DocsBot AI. |
| [Respond to Team Invite](actions/respond-to-team-invite.md) | PUT | Updates a team invite response in DocsBot AI. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from DocsBot AI. |
| [Update Team Member Role](actions/update-team-member-role.md) | PUT | Updates a team member role in DocsBot AI. |

### Team Membership

| Action | Method | Description |
| --- | --- | --- |
| [Remove Team Member or Invite](actions/remove-team-member-or-invite.md) | DELETE | Deletes a team member or invite from DocsBot AI. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in DocsBot AI. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from DocsBot AI. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from DocsBot AI. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from DocsBot AI. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in DocsBot AI. |

### Webhook Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Deep Research Webhook Test](actions/trigger-deep-research-webhook-test.md) | POST | Triggers a deep research webhook delivery test in DocsBot AI. |
| [Trigger Escalated Conversation Webhook Test](actions/trigger-escalated-conversation-webhook-test.md) | POST | Triggers an escalated conversation webhook test in DocsBot AI. |
| [Trigger Lead Webhook Test](actions/trigger-lead-webhook-test.md) | POST | Triggers a lead webhook delivery test in DocsBot AI. |
| [Trigger Rated Conversation Webhook Test](actions/trigger-rated-conversation-webhook-test.md) | POST | Triggers a rated conversation webhook test in DocsBot AI. |


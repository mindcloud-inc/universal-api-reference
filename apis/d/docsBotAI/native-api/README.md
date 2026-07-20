# DocsBot AI: Native API Reference

A consolidated summary of DocsBot AI's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docsbot.ai/documentation/developer
- **API base URL:** `https://docsbot.ai/api`

## Authentication

### API Key

Use a DocsBot user API key. DocsBot authenticates REST requests with Authorization: Bearer <API key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docsbot.ai/documentation/developer/authentication)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | `POST /teams/:teamId/bots` | [docs](https://docsbot.ai/documentation/developer/bot-api) |
| [Create Presigned Upload URL](actions/create-presigned-upload-url.md) | `GET /teams/:teamId/bots/:botId/upload-url` | [docs](https://docsbot.ai/documentation/developer/source-api) |
| [Create Source](actions/create-source.md) | `POST /teams/:teamId/bots/:botId/sources` | [docs](https://docsbot.ai/documentation/developer/source-api) |
| [Create Webhook](actions/create-webhook.md) | `POST /teams/:teamId/bots/:botId/webhooks` | [docs](https://docsbot.ai/documentation/developer/webhooks-api) |
| [Delete Bot](actions/delete-bot.md) | `DELETE /teams/:teamId/bots/:botId` | [docs](https://docsbot.ai/documentation/developer/bot-api) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE /teams/:teamId/bots/:botId/conversations/:conversationId` | [docs](https://docsbot.ai/documentation/developer/conversations-api) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /teams/:teamId/bots/:botId/leads/:leadId` | [docs](https://docsbot.ai/documentation/developer/leads-api) |
| [Delete Question](actions/delete-question.md) | `DELETE /teams/:teamId/bots/:botId/questions/:questionId` | [docs](https://docsbot.ai/documentation/developer/questions-api) |
| [Delete Source](actions/delete-source.md) | `DELETE /teams/:teamId/bots/:botId/sources/:sourceId` | [docs](https://docsbot.ai/documentation/developer/source-api) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /teams/:teamId/bots/:botId/webhooks/:webhookId` | [docs](https://docsbot.ai/documentation/developer/webhooks-api) |
| [Export Leads CSV](actions/export-leads-csv.md) | `GET /teams/:teamId/bots/:botId/leads/export` | [docs](https://docsbot.ai/documentation/developer/leads-api) |
| [Get Bot](actions/get-bot.md) | `GET /teams/:teamId/bots/:botId` | [docs](https://docsbot.ai/documentation/developer/bot-api) |
| [Get Bot Reports](actions/get-bot-reports.md) | `GET /teams/:teamId/bots/:botId/reports` | [docs](https://docsbot.ai/documentation/developer/stats-api) |
| [Get Bot Statistics](actions/get-bot-statistics.md) | `GET /teams/:teamId/bots/:botId/stats` | [docs](https://docsbot.ai/documentation/developer/stats-api) |
| [Get Conversation](actions/get-conversation.md) | `GET /teams/:teamId/bots/:botId/conversations/:conversationId` | [docs](https://docsbot.ai/documentation/developer/conversations-api) |
| [Get Research Job](actions/get-research-job.md) | `GET /teams/:teamId/bots/:botId/research/:jobId` | [docs](https://docsbot.ai/documentation/developer/bot-research-api) |
| [Get Source](actions/get-source.md) | `GET /teams/:teamId/bots/:botId/sources/:sourceId` | [docs](https://docsbot.ai/documentation/developer/source-api) |
| [Get Team](actions/get-team.md) | `GET /teams/:teamId` | [docs](https://docsbot.ai/documentation/developer/team-api) |
| [Get Webhook](actions/get-webhook.md) | `GET /teams/:teamId/bots/:botId/webhooks/:webhookId` | [docs](https://docsbot.ai/documentation/developer/webhooks-api) |
| [Invite Team Member](actions/invite-team-member.md) | `POST /teams/:teamId/invite` | [docs](https://docsbot.ai/documentation/developer/team-members-api) |
| [List Bots](actions/list-bots.md) | `GET /teams/:teamId/bots` | [docs](https://docsbot.ai/documentation/developer/bot-api) |
| [List Conversations](actions/list-conversations.md) | `GET /teams/:teamId/bots/:botId/conversations` | [docs](https://docsbot.ai/documentation/developer/conversations-api) |
| [List Leads](actions/list-leads.md) | `GET /teams/:teamId/bots/:botId/leads` | [docs](https://docsbot.ai/documentation/developer/leads-api) |
| [List Questions](actions/list-questions.md) | `GET /teams/:teamId/bots/:botId/questions` | [docs](https://docsbot.ai/documentation/developer/questions-api) |
| [List Research Jobs](actions/list-research-jobs.md) | `GET /teams/:teamId/bots/:botId/research` | [docs](https://docsbot.ai/documentation/developer/bot-research-api) |
| [List Sources](actions/list-sources.md) | `GET /teams/:teamId/bots/:botId/sources` | [docs](https://docsbot.ai/documentation/developer/source-api) |
| [List Team Members](actions/list-team-members.md) | `GET /teams/:teamId/members` | [docs](https://docsbot.ai/documentation/developer/team-members-api) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://docsbot.ai/documentation/developer/team-api) |
| [List Webhooks](actions/list-webhooks.md) | `GET /teams/:teamId/bots/:botId/webhooks` | [docs](https://docsbot.ai/documentation/developer/webhooks-api) |
| [Remove Team Member or Invite](actions/remove-team-member-or-invite.md) | `DELETE /teams/:teamId/members` | [docs](https://docsbot.ai/documentation/developer/team-members-api) |
| [Respond to Team Invite](actions/respond-to-team-invite.md) | `PUT /teams/:teamId/invite` | [docs](https://docsbot.ai/documentation/developer/team-members-api) |
| [Retry Source Indexing](actions/retry-source-indexing.md) | `PUT /teams/:teamId/bots/:botId/sources/:sourceId` | [docs](https://docsbot.ai/documentation/developer/source-api) |
| [Trigger Deep Research Webhook Test](actions/trigger-deep-research-webhook-test.md) | `POST /teams/:teamId/bots/:botId/webhooks/deliver-research` | [docs](https://docsbot.ai/documentation/developer/webhooks-api) |
| [Trigger Escalated Conversation Webhook Test](actions/trigger-escalated-conversation-webhook-test.md) | `POST /teams/:teamId/bots/:botId/webhooks/deliver-escalated` | [docs](https://docsbot.ai/documentation/developer/webhooks-api) |
| [Trigger Lead Webhook Test](actions/trigger-lead-webhook-test.md) | `POST /teams/:teamId/bots/:botId/webhooks/deliver-lead` | [docs](https://docsbot.ai/documentation/developer/webhooks-api) |
| [Trigger Rated Conversation Webhook Test](actions/trigger-rated-conversation-webhook-test.md) | `POST /teams/:teamId/bots/:botId/webhooks/deliver-rated` | [docs](https://docsbot.ai/documentation/developer/webhooks-api) |
| [Update Bot](actions/update-bot.md) | `PUT /teams/:teamId/bots/:botId` | [docs](https://docsbot.ai/documentation/developer/bot-api) |
| [Update Team](actions/update-team.md) | `PUT /teams/:teamId` | [docs](https://docsbot.ai/documentation/developer/team-api) |
| [Update Team Member Role](actions/update-team-member-role.md) | `PUT /teams/:teamId/members` | [docs](https://docsbot.ai/documentation/developer/team-members-api) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /teams/:teamId/bots/:botId/webhooks/:webhookId` | [docs](https://docsbot.ai/documentation/developer/webhooks-api) |

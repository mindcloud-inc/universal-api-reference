# <img src="https://images.mindcloud.co/apps/icons/bot-hunter_1776693354746.png" alt="BotHunter logo" width="28" height="28"> BotHunter: Universal API

Build and manage BotHunter chatbot workflows, users, and variables for Telegram, MAX, VK, and Odnoklassniki communities.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/botHunter/latest
- **Category:** Marketing / Social Media
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bothunter.ai/
- **Vendor API docs:** https://smm.targethunter.help/dev/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Community Variable](actions/get-community-variable.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/get-community-variable?connectionId=$CONNECTION_ID&varId=607d97c6a01c6a25972ed95e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Bot User

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Bot](actions/add-user-to-bot.md) | POST | Creates a BotHunter bot enrollment for a user in a specified channel. |
| [Remove User From Bot](actions/remove-user-from-bot.md) | DELETE | Deletes a BotHunter bot enrollment for a user in a specified channel. |

### Community Variable

| Action | Method | Description |
| --- | --- | --- |
| [Clear Community Variable](actions/clear-community-variable.md) | DELETE | Deletes the value of a BotHunter community variable. |
| [Get Community Variable](actions/get-community-variable.md) | GET | Retrieves a BotHunter community variable value. |
| [Set Community Variable](actions/set-community-variable.md) | PUT | Updates a BotHunter community variable value. |

### User Variable

| Action | Method | Description |
| --- | --- | --- |
| [Clear User Variable](actions/clear-user-variable.md) | DELETE | Deletes the value of a BotHunter user variable. |
| [Get User Variable](actions/get-user-variable.md) | GET | Retrieves a BotHunter user variable value. |
| [Set User Variable](actions/set-user-variable.md) | PUT | Updates a BotHunter user variable value. |


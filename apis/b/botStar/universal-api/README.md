# <img src="https://images.mindcloud.co/apps/icons/bot-star_1774634535871.png" alt="BotStar logo" width="28" height="28"> BotStar: Universal API

Build chatbots and manage bot content and audiences

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/botStar/latest
- **Category:** Support / Contact Center
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://botstar.com/
- **Vendor API docs:** https://apis.botstar.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bots](actions/list-bots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botStar/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | POST |  |
| [Get Bot](actions/get-bot.md) | GET |  |
| [List Bots](actions/list-bots.md) | GET |  |
| [Publish Bot](actions/publish-bot.md) | PUT |  |

### Bot Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot Attribute](actions/create-bot-attribute.md) | POST |  |
| [Delete Bot Attribute](actions/delete-bot-attribute.md) | DELETE |  |
| [List Bot Attributes](actions/list-bot-attributes.md) | GET |  |
| [Update Bot Attribute](actions/update-bot-attribute.md) | PUT |  |

### Cms Entity

| Action | Method | Description |
| --- | --- | --- |
| [Create CMS Entity](actions/create-cms-entity.md) | POST |  |
| [Delete CMS Entity](actions/delete-cms-entity.md) | DELETE |  |
| [Get CMS Entity](actions/get-cms-entity.md) | GET |  |
| [List CMS Entities](actions/list-cms-entities.md) | GET |  |
| [Update CMS Entity](actions/update-cms-entity.md) | PUT |  |

### Cms Entity Field

| Action | Method | Description |
| --- | --- | --- |
| [Create CMS Entity Fields](actions/create-cms-entity-fields.md) | POST |  |
| [Delete CMS Entity Fields](actions/delete-cms-entity-fields.md) | DELETE |  |
| [Update CMS Entity Fields](actions/update-cms-entity-fields.md) | PUT |  |

### Cms Entity Item

| Action | Method | Description |
| --- | --- | --- |
| [Create CMS Entity Item](actions/create-cms-entity-item.md) | POST |  |
| [Delete CMS Entity Item](actions/delete-cms-entity-item.md) | DELETE |  |
| [Get CMS Entity Item](actions/get-cms-entity-item.md) | GET |  |
| [List CMS Entity Items](actions/list-cms-entity-items.md) | GET |  |
| [Update CMS Entity Item](actions/update-cms-entity-item.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET |  |
| [Update User Attributes](actions/update-user-attributes.md) | PUT |  |

### User Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Create User Attribute](actions/create-user-attribute.md) | POST |  |


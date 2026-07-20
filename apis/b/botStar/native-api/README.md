# BotStar: Native API Reference

A consolidated summary of BotStar's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://apis.botstar.com/docs/
- **OpenAPI specification:** https://apis.botstar.com/docs/public-api.yaml
- **API base URL:** `https://apis.botstar.com/v1`

## Authentication

### API Token

Use the API Token from your BotStar account profile.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apis.botstar.com/docs/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | `POST /bots/` | [docs](https://apis.botstar.com/docs/#/Bots/post_bots_) |
| [Create Bot Attribute](actions/create-bot-attribute.md) | `POST /bots/:botId/attributes` | [docs](https://apis.botstar.com/docs/#/Bots/post_bots__botId__attributes) |
| [Create CMS Entity](actions/create-cms-entity.md) | `POST /bots/:botId/cms_entities` | [docs](https://apis.botstar.com/docs/#/CMS%20Entities/post_bots__botId__cms_entities) |
| [Create CMS Entity Fields](actions/create-cms-entity-fields.md) | `POST /bots/:botId/cms_entities/:entityId/fields` | [docs](https://apis.botstar.com/docs/#/CMS%20Entity%20Fields/post_bots__botId__cms_entities__entityId__fields) |
| [Create CMS Entity Item](actions/create-cms-entity-item.md) | `POST /bots/:botId/cms_entities/:entityId/items` | [docs](https://apis.botstar.com/docs/#/CMS%20Entity%20Items/post_bots__botId__cms_entities__entityId__items) |
| [Create User Attribute](actions/create-user-attribute.md) | `POST /bots/:botId/users/attributes` | [docs](https://apis.botstar.com/docs/#/Users/post_bots__botId__users_attributes) |
| [Delete Bot Attribute](actions/delete-bot-attribute.md) | `DELETE /bots/:botId/attributes/:attributeId` | [docs](https://apis.botstar.com/docs/#/Bots/delete_bots__botId__attributes__attributeId_) |
| [Delete CMS Entity](actions/delete-cms-entity.md) | `DELETE /bots/:botId/cms_entities/:entityId` | [docs](https://apis.botstar.com/docs/#/CMS%20Entities/delete_bots__botId__cms_entities__entityId_) |
| [Delete CMS Entity Fields](actions/delete-cms-entity-fields.md) | `DELETE /bots/:botId/cms_entities/:entityId/fields` | [docs](https://apis.botstar.com/docs/#/CMS%20Entity%20Fields/delete_bots__botId__cms_entities__entityId__fields) |
| [Delete CMS Entity Item](actions/delete-cms-entity-item.md) | `DELETE /bots/:botId/cms_entities/:entityId/items/:entityItemId` | [docs](https://apis.botstar.com/docs/#/CMS%20Entity%20Items/delete_bots__botId__cms_entities__entityId__items__entityItemId_) |
| [Get Bot](actions/get-bot.md) | `GET /bots/:botId` | [docs](https://apis.botstar.com/docs/#/Bots/get_bots__botId_) |
| [Get CMS Entity](actions/get-cms-entity.md) | `GET /bots/:botId/cms_entities/:entityId` | [docs](https://apis.botstar.com/docs/#/CMS%20Entities/get_bots__botId__cms_entities__entityId_) |
| [Get CMS Entity Item](actions/get-cms-entity-item.md) | `GET /bots/:botId/cms_entities/:entityId/items/:entityItemId` | [docs](https://apis.botstar.com/docs/#/CMS%20Entity%20Items/get_bots__botId__cms_entities__entityId__items__entityItemId_) |
| [Get User Info](actions/get-user-info.md) | `GET /bots/:botId/users/:userId` | [docs](https://apis.botstar.com/docs/#/Users/get_bots__botId__users__userId_) |
| [List Bot Attributes](actions/list-bot-attributes.md) | `GET /bots/:botId/attributes` | [docs](https://apis.botstar.com/docs/#/Bots/get_bots__botId__attributes) |
| [List Bots](actions/list-bots.md) | `GET /bots/` | [docs](https://apis.botstar.com/docs/#/Bots/get_bots_) |
| [List CMS Entities](actions/list-cms-entities.md) | `GET /bots/:botId/cms_entities` | [docs](https://apis.botstar.com/docs/#/CMS%20Entities/get_bots__botId__cms_entities) |
| [List CMS Entity Items](actions/list-cms-entity-items.md) | `GET /bots/:botId/cms_entities/:entityId/items` | [docs](https://apis.botstar.com/docs/#/CMS%20Entity%20Items/get_bots__botId__cms_entities__entityId__items) |
| [Publish Bot](actions/publish-bot.md) | `POST /bots/:botId/publish` | [docs](https://apis.botstar.com/docs/#/Bots/post_bots__botId__publish) |
| [Update Bot Attribute](actions/update-bot-attribute.md) | `PATCH /bots/:botId/attributes/:attributeId` | [docs](https://apis.botstar.com/docs/#/Bots/patch_bots__botId__attributes__attributeId_) |
| [Update CMS Entity](actions/update-cms-entity.md) | `PATCH /bots/:botId/cms_entities/:entityId` | [docs](https://apis.botstar.com/docs/#/CMS%20Entities/patch_bots__botId__cms_entities__entityId_) |
| [Update CMS Entity Fields](actions/update-cms-entity-fields.md) | `PATCH /bots/:botId/cms_entities/:entityId/fields` | [docs](https://apis.botstar.com/docs/#/CMS%20Entity%20Fields/patch_bots__botId__cms_entities__entityId__fields) |
| [Update CMS Entity Item](actions/update-cms-entity-item.md) | `PATCH /bots/:botId/cms_entities/:entityId/items/:entityItemId` | [docs](https://apis.botstar.com/docs/#/CMS%20Entity%20Items/patch_bots__botId__cms_entities__entityId__items__entityItemId_) |
| [Update User Attributes](actions/update-user-attributes.md) | `PATCH /bots/:botId/users/:userId` | [docs](https://apis.botstar.com/docs/#/Users/patch_bots__botId__users__userId_) |

# <img src="https://images.mindcloud.co/apps/icons/idh-hq-zx-le5-logos_1773161920130.png" alt="ManyChat logo" width="28" height="28"> ManyChat: Universal API

Manage subscribers, tags, fields, and messaging flows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/manyChat/latest
- **Category:** Marketing
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://manychat.com
- **Vendor API docs:** https://api.manychat.com/swagger

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Page Info](actions/get-page-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyChat/latest/actions/get-page-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Bot Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot Field](actions/create-bot-field.md) | POST | Creates a new bot field in ManyChat. |
| [List Bot Fields](actions/list-bot-fields.md) | GET | Retrieves page bot fields from ManyChat. |
| [Set Bot Field](actions/set-bot-field.md) | PUT | Updates an existing bot field in ManyChat. |
| [Set Bot Fields](actions/set-bot-fields.md) | PUT | Updates multiple bot fields in ManyChat. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in ManyChat. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves page custom fields from ManyChat. |

### Flow

| Action | Method | Description |
| --- | --- | --- |
| [List Flows](actions/list-flows.md) | GET | Retrieves page flows from ManyChat. |

### Growth Tool

| Action | Method | Description |
| --- | --- | --- |
| [List Growth Tools](actions/list-growth-tools.md) | GET | Retrieves growth tools from ManyChat. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Content](actions/send-content.md) | POST | Sends content to a subscriber in ManyChat. |
| [Send Flow](actions/send-flow.md) | POST | Sends an automation flow in ManyChat. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Info](actions/get-page-info.md) | GET | Retrieves connected page details from ManyChat. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag To Subscriber](actions/add-tag-to-subscriber.md) | PUT | Adds a tag to a subscriber in ManyChat. |
| [Add Tag To Subscriber By Name](actions/add-tag-to-subscriber-by-name.md) | PUT | Adds a tag to a subscriber in ManyChat by name. |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in ManyChat. |
| [Get Subscriber Info](actions/get-subscriber-info.md) | GET | Retrieves a subscriber from ManyChat. |
| [Get Subscriber Info By User Ref](actions/get-subscriber-info-by-user-ref.md) | GET | Finds a subscriber in ManyChat by user ref. |
| [Remove Tag From Subscriber](actions/remove-tag-from-subscriber.md) | PUT | Removes a tag from a subscriber in ManyChat. |
| [Remove Tag From Subscriber By Name](actions/remove-tag-from-subscriber-by-name.md) | PUT | Removes a tag from a subscriber in ManyChat by name. |
| [Search Subscribers by Custom Field](actions/search-subscribers-by-custom-field.md) | GET | Finds subscribers in ManyChat by custom field. |
| [Search Subscribers by Name](actions/search-subscribers-by-name.md) | GET | Finds subscribers in ManyChat by name. |
| [Search Subscribers by System Field](actions/search-subscribers-by-system-field.md) | GET | Finds subscribers in ManyChat by system field. |
| [Set Subscriber Custom Field](actions/set-subscriber-custom-field.md) | PUT | Updates a subscriber custom field in ManyChat. |
| [Set Subscriber Custom Field By Name](actions/set-subscriber-custom-field-by-name.md) | PUT | Updates a subscriber custom field in ManyChat by name. |
| [Set Subscriber Custom Fields](actions/set-subscriber-custom-fields.md) | PUT | Updates subscriber custom fields in ManyChat. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in ManyChat. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in ManyChat. |
| [List Tags](actions/list-tags.md) | GET | Retrieves available page tags from ManyChat. |
| [Remove Tag](actions/remove-tag.md) | DELETE | Deletes an existing tag from ManyChat. |


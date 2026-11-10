# <img src="https://images.mindcloud.co/apps/icons/ehs-insight-icon_1782393296786.png" alt="EHS Insight logo" width="28" height="28"> EHS Insight: Universal API

EHS Insight through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ehsInsight/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Business Entity](actions/get-business-entity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/get-business-entity?connectionId=$CONNECTION_ID&rowUid=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Business Entity

| Action | Method | Description |
| --- | --- | --- |
| [Create Business Entity](actions/create-business-entity.md) | POST |  |
| [Get Business Entity](actions/get-business-entity.md) | GET |  |
| [List Business Entities](actions/list-business-entities.md) | GET |  |
| [Update Business Entity](actions/update-business-entity.md) | PUT |  |

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [List Entities](actions/list-entities.md) | GET |  |
| [Get Entity Schema](actions/new-action1.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Entity](actions/add-entity.md) | POST |  |
| [Create User Contact](actions/create-user-contact.md) | POST |  |
| [Get Entity Items](actions/get-entity-items.md) | GET |  |
| [Get Single Item](actions/get-single-item.md) | GET |  |
| [Update Entity](actions/update-entity.md) | PUT |  |
| [Update User Contact](actions/update-user-contact.md) | PUT | Warning: This endpoint doesn't allow partial updates, you need to pass all values to avoid data loss |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET |  |
| [List User Contacts](actions/list-user-contacts.md) | GET |  |


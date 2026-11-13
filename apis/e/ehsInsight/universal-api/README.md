# <img src="https://images.mindcloud.co/apps/icons/ehs-insight-icon_1782393296786.png" alt="EHS Insight logo" width="28" height="28"> EHS Insight: Universal API

EHS Insight through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ehsInsight/latest
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Attachment](actions/get-attachment.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/get-attachment?connectionId=$CONNECTION_ID&rowUid=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment](actions/get-attachment.md) | GET |  |
| [Get SDS Community Attachment](actions/get-sds-community-attachment.md) | GET |  |
| [Upload Attachment](actions/upload-attachment.md) | POST |  |

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
| [Get Single Item](actions/get-single-item.md) | GET |  |
| [List Entity Items](actions/list-entity-items.md) | GET |  |
| [Update Entity](actions/update-entity.md) | PUT |  |

### User Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create User Contact](actions/create-user-contact.md) | POST |  |
| [Delete User Contact](actions/delete-user-contact.md) | DELETE |  |
| [Get User Contact](actions/get-user-contact.md) | GET |  |
| [List User Contacts with Parameters](actions/list-user-contacts-with-parameters.md) | GET |  |
| [Update User Contact](actions/update-user-contact.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET |  |


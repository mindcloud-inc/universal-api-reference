# <img src="https://images.mindcloud.co/apps/icons/knack_1773425496533.png" alt="Knack logo" width="28" height="28"> Knack: Universal API

Build databases, portals, and workflows with Knack

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/knack/latest
- **Category:** IT Operations / Database
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.knack.com
- **Vendor API docs:** https://docs.knack.com/v3/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Records](actions/list-records.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/knack/latest/actions/list-records?connectionId=$CONNECTION_ID&objectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Upload File Image Asset](actions/upload-file-image-asset.md) | POST |  |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST |  |
| [Delete Record](actions/delete-record.md) | DELETE |  |
| [Get Record By ID](actions/get-record-by-id.md) | GET |  |
| [List Records](actions/list-records.md) | GET |  |
| [Update Record](actions/update-record.md) | PUT |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Remote User Login](actions/create-remote-user-login.md) | POST |  |

### User Account

| Action | Method | Description |
| --- | --- | --- |
| [Create User Account Record](actions/create-user-account-record.md) | POST |  |
| [Update User Account Record](actions/update-user-account-record.md) | PUT |  |
| [Update User Roles On Account](actions/update-user-roles-on-account.md) | PUT |  |


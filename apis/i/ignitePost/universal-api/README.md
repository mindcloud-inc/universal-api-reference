# <img src="https://images.mindcloud.co/apps/icons/images_1774903014323.jpeg" alt="IgnitePost logo" width="28" height="28"> IgnitePost: Universal API

Create, preview, and track handwritten card orders

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ignitePost/latest
- **Category:** Marketing
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ignitepost.com
- **Vendor API docs:** https://dashboard.ignitepost.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Authenticate](actions/authenticate.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/authenticate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Default Image

| Action | Method | Description |
| --- | --- | --- |
| [List Default Images](actions/list-default-images.md) | GET | Retrieves available default images from IgnitePost. |

### Font

| Action | Method | Description |
| --- | --- | --- |
| [List Fonts](actions/list-fonts.md) | GET | Retrieves available handwriting fonts from IgnitePost. |

### Insert

| Action | Method | Description |
| --- | --- | --- |
| [List Inserts](actions/list-inserts.md) | GET | Retrieves available gift card inserts from IgnitePost. |

### Letter Template

| Action | Method | Description |
| --- | --- | --- |
| [List Letter Templates](actions/list-letter-templates.md) | GET | Retrieves available letter templates from IgnitePost. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Preview Note](actions/preview-note.md) | GET | Retrieves preview image URLs for a note in IgnitePost. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in IgnitePost. |
| [Retrieve Order](actions/retrieve-order.md) | GET | Retrieves an existing order from IgnitePost. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | GET | Tests your IgnitePost authentication and returns your account email. |


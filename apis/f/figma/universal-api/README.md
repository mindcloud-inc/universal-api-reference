# <img src="https://images.mindcloud.co/apps/icons/figma_1772206602324.png" alt="Figma logo" width="28" height="28"> Figma: Universal API

Design interfaces, prototype flows, collaborate with teams, and ship products.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/figma/latest
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.figma.com/
- **Vendor API docs:** https://developers.figma.com/docs/rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Component](actions/get-component.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-component?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create File Comment](actions/create-file-comment.md) | POST | Creates a new comment in a Figma file. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [List File Comments](actions/list-file-comments.md) | GET | Retrieves comments from a Figma file. |

### Component

| Action | Method | Description |
| --- | --- | --- |
| [Get Component](actions/get-component.md) | GET | Retrieves a component from Figma by key. |

### Component Set

| Action | Method | Description |
| --- | --- | --- |
| [Get Component Set](actions/get-component-set.md) | GET | Retrieves a component set from Figma by key. |

### Component Sets

| Action | Method | Description |
| --- | --- | --- |
| [List File Component Sets](actions/list-file-component-sets.md) | GET | Retrieves component sets from a Figma file. |

### Components

| Action | Method | Description |
| --- | --- | --- |
| [List File Components](actions/list-file-components.md) | GET | Retrieves components from a Figma file. |

### Dev Resource

| Action | Method | Description |
| --- | --- | --- |
| [List File Dev Resources](actions/list-file-dev-resources.md) | GET | Retrieves dev resources from a Figma file. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET | Retrieves a Figma file by key. |

### File Images

| Action | Method | Description |
| --- | --- | --- |
| [Get File Images](actions/get-file-images.md) | GET | Retrieves image fills from a Figma file. |

### File Nodes

| Action | Method | Description |
| --- | --- | --- |
| [Get File Nodes](actions/get-file-nodes.md) | GET | Retrieves nodes from a Figma file by ID. |

### File Versions

| Action | Method | Description |
| --- | --- | --- |
| [List File Versions](actions/list-file-versions.md) | GET | Retrieves version history from a Figma file. |

### Rendered Images

| Action | Method | Description |
| --- | --- | --- |
| [Get Rendered Images](actions/get-rendered-images.md) | GET | Retrieves rendered images from a Figma file. |

### Style

| Action | Method | Description |
| --- | --- | --- |
| [Get Style](actions/get-style.md) | GET | Retrieves a style from Figma by key. |

### Styles

| Action | Method | Description |
| --- | --- | --- |
| [List File Styles](actions/list-file-styles.md) | GET | Retrieves styles from a Figma file. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the authenticated user from Figma. |

### Variable

| Action | Method | Description |
| --- | --- | --- |
| [Get Local Variables](actions/get-local-variables.md) | GET | Retrieves local variables from a Figma file. |
| [Get Published Variables](actions/get-published-variables.md) | GET | Retrieves published variables from a Figma file. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Figma. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Figma. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Figma. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Figma. |


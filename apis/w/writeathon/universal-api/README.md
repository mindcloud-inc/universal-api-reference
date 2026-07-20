# <img src="https://images.mindcloud.co/apps/icons/writeathon_1775161243181.png" alt="Writeathon logo" width="28" height="28"> Writeathon: Universal API

Create and organize Writeathon cards, spaces, and writing picks through the official Writeathon integration API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/writeathon/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.writeathon.cn
- **Vendor API docs:** https://guide.writeathon.cn/help/tools/api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Append Card](actions/append-card.md) | PUT | Appends content to an existing Writeathon card. |
| [Create Card](actions/create-card.md) | POST | Creates a new card in Writeathon. |
| [Create Card With Attachments](actions/create-card-with-attachments.md) | POST | Creates a new Writeathon card with attachments. |
| [Extend Card](actions/extend-card.md) | POST | Creates a child card under a Writeathon card. |
| [Extend Card With Attachments](actions/extend-card-with-attachments.md) | POST | Creates a child card with attachments in Writeathon. |
| [Get Card By ID](actions/get-card-by-id.md) | GET | Retrieves a Writeathon card by ID. |
| [Get Card By Title](actions/get-card-by-title.md) | GET | Retrieves a Writeathon card by title. |
| [Get Recent Cards](actions/get-recent-cards.md) | GET | Retrieves recently updated cards from Writeathon. |
| [Get Writing Picks](actions/get-writing-picks.md) | GET | Retrieves writing picks from the current Writeathon account. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Writeathon. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves the user's spaces from Writeathon. |


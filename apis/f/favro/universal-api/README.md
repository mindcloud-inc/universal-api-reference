# <img src="https://images.mindcloud.co/apps/icons/favro_1775769580591.png" alt="Favro logo" width="28" height="28"> Favro: Universal API

Plan work, manage boards, roadmaps, cards, and collaboration workflows in Favro.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/favro/latest
- **Category:** Productivity / Project Management
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.favro.com/
- **Vendor API docs:** https://favro.com/developer/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organizations](actions/get-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Backlog Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Card](actions/create-card.md) | POST | Creates a new card in Favro. |
| [Delete Card](actions/delete-card.md) | DELETE | Deletes an existing card from Favro. |
| [Get All Cards](actions/get-all-cards.md) | GET | Retrieves cards from Favro. |
| [Get Card](actions/get-card.md) | GET | Retrieves a card from Favro by card ID. |
| [Update Card](actions/update-card.md) | PUT | Updates an existing card in Favro. |

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Create Widget](actions/create-widget.md) | POST | Creates a new widget in Favro. |
| [Delete Widget](actions/delete-widget.md) | DELETE | Deletes an existing widget from Favro. |
| [Get All Widgets](actions/get-all-widgets.md) | GET | Retrieves widgets from Favro. |
| [Get Widget](actions/get-widget.md) | GET | Retrieves a widget from Favro by widget ID. |
| [Update Widget](actions/update-widget.md) | PUT | Updates an existing widget in Favro. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Favro. |
| [Delete Collection](actions/delete-collection.md) | DELETE | Deletes an existing collection from Favro. |
| [Get All Collections](actions/get-all-collections.md) | GET | Retrieves collections from Favro. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection from Favro by collection ID. |
| [Update Collection](actions/update-collection.md) | PUT | Updates an existing collection in Favro. |

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [Get All Columns](actions/get-all-columns.md) | GET | Retrieves columns from Favro. |
| [Get Column](actions/get-column.md) | GET | Retrieves a column from Favro by column ID. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organizations](actions/get-organizations.md) | GET | Retrieves organizations from Favro. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get All Users](actions/get-all-users.md) | GET | Retrieves users from Favro. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Favro by user ID. |


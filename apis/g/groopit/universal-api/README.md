# <img src="https://images.mindcloud.co/apps/icons/letsgroopit-logo_1775571471619.jpeg" alt="Groopit logo" width="28" height="28"> Groopit: Universal API

Groopit OData wrapper for assignment and post feeds.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/groopit/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://groopit.co
- **Vendor API docs:** https://groopit.co/help-center/tips-tricks/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Assignments](actions/list-assignments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/groopit/latest/actions/list-assignments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Get Assignment](actions/get-assignment.md) | GET |  |
| [List Assignments](actions/list-assignments.md) | GET |  |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Assignment Post](actions/get-assignment-post.md) | GET |  |
| [List Assignment Posts](actions/list-assignment-posts.md) | GET |  |


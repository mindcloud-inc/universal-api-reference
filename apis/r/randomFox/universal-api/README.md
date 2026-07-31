# <img src="https://images.mindcloud.co/apps/icons/random-fox_1785361474451.png" alt="RandomFox logo" width="28" height="28"> RandomFox: Universal API

Retrieve random fox-image URLs and their shareable RandomFox page links.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/randomFox/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://randomfox.ca/
- **Vendor API docs:** https://randomfox.ca/floof/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Random Fox](actions/get-random-fox.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomFox/latest/actions/get-random-fox?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Fox

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Fox](actions/get-random-fox.md) | GET |  |
| [Get Random Foxes](actions/get-random-foxes.md) | GET |  |


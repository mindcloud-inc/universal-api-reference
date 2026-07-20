# <img src="https://images.mindcloud.co/apps/icons/shorten-rest_1774546490823.png" alt="Shorten.REST logo" width="28" height="28"> Shorten.REST: Universal API

Create and manage shortened URLs, destination rules, metatags, snippets, and click data in Shorten.REST.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shortenREST/latest
- **Category:** Marketing
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shorten.rest/
- **Vendor API docs:** https://docs.shorten.rest/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Aliases by Domain](actions/list-aliases-by-domain.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortenREST/latest/actions/list-aliases-by-domain?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Alias

| Action | Method | Description |
| --- | --- | --- |
| [Create Alias](actions/create-alias.md) | POST | Creates a new alias in Shorten.REST. |
| [Delete Alias](actions/delete-alias.md) | DELETE | Deletes an existing alias from Shorten.REST. |
| [Get Alias](actions/get-alias.md) | GET | Retrieves alias details from Shorten.REST by alias and domain. |
| [List Aliases by Domain](actions/list-aliases-by-domain.md) | GET | Retrieves aliases from Shorten.REST for a specific domain. |
| [Update Alias](actions/update-alias.md) | PUT | Updates an existing alias in Shorten.REST. |

### Click

| Action | Method | Description |
| --- | --- | --- |
| [List Clicks](actions/list-clicks.md) | GET | Retrieves raw click data from Shorten.REST. |


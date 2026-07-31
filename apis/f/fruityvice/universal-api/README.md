# <img src="https://images.mindcloud.co/apps/icons/fruityvice_1785420750484.png" alt="Fruityvice logo" width="28" height="28"> Fruityvice: Universal API

Retrieve botanical and nutritional data for fruits, measured per 100 grams.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fruityvice/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fruityvice.com/
- **Vendor API docs:** https://www.fruityvice.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get fruit by ID](actions/get-fruit-by-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fruityvice/latest/actions/get-fruit-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Fruit

| Action | Method | Description |
| --- | --- | --- |
| [Get fruit by ID](actions/get-fruit-by-id.md) | GET |  |
| [Get fruit by name](actions/get-fruit-by-name.md) | GET |  |
| [List fruits](actions/list-fruits.md) | GET |  |


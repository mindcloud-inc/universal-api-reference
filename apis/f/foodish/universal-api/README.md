# <img src="https://images.mindcloud.co/apps/icons/foodish_1785427041260.png" alt="Foodish logo" width="28" height="28"> Foodish: Universal API

Foodish through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/foodish/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Food Image by Category](actions/get-food-image-by-category.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foodish/latest/actions/get-food-image-by-category?connectionId=$CONNECTION_ID&category=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Food Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Food Image by Category](actions/get-food-image-by-category.md) | GET |  |
| [Get Random Food Image](actions/get-random-food-image.md) | GET |  |


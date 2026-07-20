# <img src="https://images.mindcloud.co/apps/icons/placedog_1777911493909.png" alt="Placedog logo" width="28" height="28"> Placedog: Universal API

Generate placeholder dog images for websites and projects

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/placedog/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://placedog.net
- **Vendor API docs:** https://placedog.net/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Images](actions/list-images.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placedog/latest/actions/list-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Blurred Placeholder Image](actions/get-blurred-placeholder-image.md) | GET | Retrieves a blurred placeholder dog image from Placedog. |
| [Get Filtered Placeholder Image](actions/get-filtered-placeholder-image.md) | GET | Retrieves a filtered placeholder dog image from Placedog. |
| [Get Filtered Specific Image](actions/get-filtered-specific-image.md) | GET | Retrieves a filtered Placedog image by image ID. |
| [Get Greyscale Placeholder Image](actions/get-greyscale-placeholder-image.md) | GET | Retrieves a greyscale placeholder dog image from Placedog. |
| [Get Placeholder Image](actions/get-placeholder-image.md) | GET | Retrieves a placeholder dog image from Placedog by width. |
| [Get Placeholder Image By Dimensions](actions/get-placeholder-image-by-dimensions.md) | GET | Retrieves a placeholder dog image from Placedog by width and height. |
| [Get Placeholder Image By X Dimensions](actions/get-placeholder-image-by-x-dimensions.md) | GET | Retrieves a placeholder dog image from Placedog using x dimensions. |
| [Get Random Placeholder Image](actions/get-random-placeholder-image.md) | GET | Retrieves a random placeholder dog image from Placedog. |
| [Get Specific Image](actions/get-specific-image.md) | GET | Retrieves a specific Placedog image by image ID. |
| [List Images](actions/list-images.md) | GET | Retrieves available Placedog image IDs and attribution details. |


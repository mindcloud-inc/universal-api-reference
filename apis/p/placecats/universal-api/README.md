# <img src="https://images.mindcloud.co/apps/icons/placecats_1785420656809.png" alt="Placecats logo" width="28" height="28"> Placecats: Universal API

Read public random, named, and grayscale cat placeholder images with documented dimensions, fit, and position options.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/placecats/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://placecats.com/
- **Vendor API docs:** https://placecats.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Grayscale Cat Placeholder](actions/get-grayscale-cat-placeholder.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placecats/latest/actions/get-grayscale-cat-placeholder?connectionId=$CONNECTION_ID&width=1&height=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Cat Placeholder Media

| Action | Method | Description |
| --- | --- | --- |
| [Get Grayscale Cat Placeholder](actions/get-grayscale-cat-placeholder.md) | GET |  |
| [Get Random Cat Placeholder](actions/get-random-cat-placeholder.md) | GET |  |
| [Get Specific Cat Placeholder](actions/get-specific-cat-placeholder.md) | GET |  |


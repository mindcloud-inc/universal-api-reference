# <img src="https://images.mindcloud.co/apps/icons/robohash_1777545725229.png" alt="Robohash logo" width="28" height="28"> Robohash: Universal API

Robohash generates deterministic avatar images from text using a public URL-based HTTP service, with optional image format, size, robot set, background, Gravatar, and extension-handling parameters.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/robohash/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://robohash.org/
- **Vendor API docs:** https://github.com/e1ven/Robohash

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Image](actions/generate-image.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/robohash/latest/actions/generate-image?connectionId=$CONNECTION_ID&text=user%40example.com&format=png" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Generated Image

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | GET |  |


# <img src="https://images.mindcloud.co/apps/icons/vadivelu-httpcodes_1785358330080.png" alt="Vadivelu HTTP codes logo" width="28" height="28"> Vadivelu HTTP codes: Universal API

Retrieve Vadivelu fan-project images for documented HTTP status codes.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vadiveluHTTPCodes/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vadivelu.anoram.com/
- **Vendor API docs:** https://vadivelu.anoram.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get GIF Status Code Image](actions/get-gif-status-code-image.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vadiveluHTTPCodes/latest/actions/get-gif-status-code-image?connectionId=$CONNECTION_ID&statusCode=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Http Status Code Image

| Action | Method | Description |
| --- | --- | --- |
| [Get GIF Status Code Image](actions/get-gif-status-code-image.md) | GET |  |
| [Get JPG Status Code Image](actions/get-jpg-status-code-image.md) | GET |  |


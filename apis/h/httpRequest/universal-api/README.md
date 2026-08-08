# HTTP: Universal API

Make an HTTP(s) request to a given URL and handle the returned response.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/httpRequest/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send HTTP Request](actions/send-http-request.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/httpRequest/latest/actions/send-http-request?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fpath%3Fquery%3Dvalue&method=DELETE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Send HTTP Request](actions/send-http-request.md) | GET | Sends an HTTP request to any URL. |


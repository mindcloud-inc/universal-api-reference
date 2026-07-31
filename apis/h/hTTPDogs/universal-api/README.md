# <img src="https://images.mindcloud.co/apps/icons/h-ttpdogs_1785360528410.png" alt="HTTP Dogs logo" width="28" height="28"> HTTP Dogs: Universal API

Read HTTP status dog representations as JPEG, WebP, JXL, AVIF, or JSON.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hTTPDogs/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://http.dog/
- **Vendor API docs:** https://http.dog/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get HTTP Status Dog AVIF](actions/get-http-status-dog-avif.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hTTPDogs/latest/actions/get-http-status-dog-avif?connectionId=$CONNECTION_ID&statusCode=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Http Status Dog

| Action | Method | Description |
| --- | --- | --- |
| [Get HTTP Status Dog AVIF](actions/get-http-status-dog-avif.md) | GET |  |
| [Get HTTP Status Dog JPEG](actions/get-http-status-dog-jpeg.md) | GET |  |
| [Get HTTP Status Dog JSON](actions/get-http-status-dog-json.md) | GET |  |
| [Get HTTP Status Dog JXL](actions/get-http-status-dog-jxl.md) | GET |  |
| [Get HTTP Status Dog WebP](actions/get-http-status-dog-webp.md) | GET |  |


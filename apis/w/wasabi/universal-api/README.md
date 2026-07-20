# <img src="https://images.mindcloud.co/apps/icons/images-26_1776872457622.png" alt="Wasabi logo" width="28" height="28"> Wasabi: Universal API

S3-compatible object storage by Wasabi Technologies for managing buckets and objects.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wasabi/latest
- **Category:** Content & Files / Storage
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wasabi.com
- **Vendor API docs:** https://docs.wasabi.com/apidocs/wasabi-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Buckets](actions/list-buckets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/list-buckets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Objects](actions/list-objects.md) | GET | Retrieves objects from a specific bucket in Wasabi. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Bucket](actions/create-bucket.md) | POST | Creates a new bucket in Wasabi. |
| [List Buckets](actions/list-buckets.md) | GET | Retrieves the buckets available in your Wasabi account. |


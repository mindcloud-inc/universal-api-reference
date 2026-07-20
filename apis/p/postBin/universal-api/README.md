# <img src="https://images.mindcloud.co/apps/icons/post-bin_1775829058100.png" alt="PostBin logo" width="28" height="28"> PostBin: Universal API

Capture and inspect temporary HTTP request bins with the public PostBin API for webhook and request testing.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/postBin/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.postb.in
- **Vendor API docs:** https://www.postb.in/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Bin](actions/get-bin.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postBin/latest/actions/get-bin?connectionId=$CONNECTION_ID&binId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Bin

| Action | Method | Description |
| --- | --- | --- |
| [Create Bin](actions/create-bin.md) | POST | Creates a new PostBin bin. |
| [Delete Bin](actions/delete-bin.md) | DELETE | Deletes a PostBin bin and its requests. |
| [Get Bin](actions/get-bin.md) | GET | Retrieves a PostBin bin by ID. |

### Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Request](actions/get-request.md) | GET | Retrieves a stored request from a PostBin bin. |
| [Shift Request](actions/shift-request.md) | GET | Retrieves and removes the oldest request from a PostBin bin. |


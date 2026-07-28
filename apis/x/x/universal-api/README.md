# <img src="https://mindcloud.imgix.net/apps/icons/x_1772680913587.png" alt="X logo" width="28" height="28"> X: Universal API

X (formerly Twitter) API integration for posting and managing content.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/x/latest
- **Category:** Marketing
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://x.com
- **Vendor API docs:** https://docs.x.com/x-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/x/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET |  |


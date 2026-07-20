# <img src="https://images.mindcloud.co/apps/icons/share_1775145209655.png" alt="DOOMSCROLLR logo" width="28" height="28"> DOOMSCROLLR: Universal API

DOOMSCROLLR content and audience API for tenant-scoped publishing workflows using query-parameter API key auth.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dOOMSCROLLR/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://doomscrollr.com
- **Vendor API docs:** https://doomscrollr.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Content Posts](actions/list-content-posts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/list-content-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Api Key Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify API Key](actions/verify-api-key.md) | GET |  |

### Audience Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Audience Member](actions/create-audience-member.md) | POST |  |
| [List Audience Members](actions/list-audience-members.md) | GET |  |

### Content Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Content Post](actions/create-content-post.md) | POST |  |
| [List Content Posts](actions/list-content-posts.md) | GET |  |


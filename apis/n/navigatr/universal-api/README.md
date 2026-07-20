# <img src="https://images.mindcloud.co/apps/icons/navigatr_1777053591399.png" alt="Navigatr logo" width="28" height="28"> Navigatr: Universal API

Create, issue, and manage digital badges and learning pathways

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/navigatr/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.navigatr.org
- **Vendor API docs:** https://api.navigatr.app/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Detail](actions/get-user-detail.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/get-user-detail?connectionId=$CONNECTION_ID&userId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Badge

| Action | Method | Description |
| --- | --- | --- |
| [List Badge Assertions](actions/list-badge-assertions.md) | GET |  |
| [List Badges](actions/list-badges.md) | GET |  |

### Badge Assertion

| Action | Method | Description |
| --- | --- | --- |
| [List User Badges](actions/list-user-badges.md) | GET |  |

### Community

| Action | Method | Description |
| --- | --- | --- |
| [List User Communities](actions/list-user-communities.md) | GET |  |

### User Detail

| Action | Method | Description |
| --- | --- | --- |
| [Get User Detail](actions/get-user-detail.md) | GET | Retrieves user details from Navigatr. |


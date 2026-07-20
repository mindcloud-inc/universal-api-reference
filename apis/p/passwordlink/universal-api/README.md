# <img src="https://images.mindcloud.co/apps/icons/passwordlink_1776713057446.png" alt="Password.link logo" width="28" height="28"> Password.link: Universal API

Password.link API wrapper for encrypted one-time secrets and secret requests.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/passwordlink/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://password.link/en
- **Vendor API docs:** https://password.link/en/p/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Secrets](actions/list-secrets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/list-secrets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Secret

| Action | Method | Description |
| --- | --- | --- |
| [Create Secret](actions/create-secret.md) | POST |  |
| [Delete Secret](actions/delete-secret.md) | DELETE |  |
| [List Secrets](actions/list-secrets.md) | GET |  |
| [View Secret](actions/view-secret.md) | GET |  |

### Secret Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Secret Request](actions/create-secret-request.md) | POST |  |
| [Delete Secret Request](actions/delete-secret-request.md) | DELETE |  |
| [List Secret Requests](actions/list-secret-requests.md) | GET |  |


# <img src="https://images.mindcloud.co/apps/icons/onceto_1774978967690.png" alt="Once.to logo" width="28" height="28"> Once.to: Universal API

Create short links and manage domains

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/onceto/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://once.to
- **Vendor API docs:** https://docs.once.to/en/api/v1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceto/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain](actions/get-domain.md) | GET | Retrieves a domain from Once.to. |
| [List Domains](actions/list-domains.md) | GET | Retrieves all domains from Once.to. |
| [Update Domain Settings](actions/update-domain-settings.md) | PUT | Updates an existing domain in Once.to. |

### Short Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Short Link](actions/create-short-link.md) | POST | Creates a new short link in Once.to. |
| [Get Link](actions/get-link.md) | GET | Retrieves a short link from Once.to. |
| [List Links](actions/list-links.md) | GET | Retrieves all short links from Once.to. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Once.to. |


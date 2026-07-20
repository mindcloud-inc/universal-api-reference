# <img src="https://images.mindcloud.co/apps/icons/n-mkr_1776114297982.png" alt="NMKR logo" width="28" height="28"> NMKR: Universal API

Create, mint, and manage NFTs and tokenized assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nMKR/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://studio.nmkr.io
- **Vendor API docs:** https://docs.nmkr.io/nmkr-studio-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nMKR/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves all your projects from NMKR. |


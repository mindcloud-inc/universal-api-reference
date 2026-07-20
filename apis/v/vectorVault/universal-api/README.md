# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-10-as-09_1775823767806.png" alt="Vector Vault logo" width="28" height="28"> Vector Vault: Universal API

Search, chat, and manage AI knowledge vaults

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vectorVault/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vectorvault.io
- **Vendor API docs:** https://github.com/John-Rood/VectorVault/tree/main/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Vaults](actions/list-vaults.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectorVault/latest/actions/list-vaults?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Vaults](actions/list-vaults.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | POST |  |


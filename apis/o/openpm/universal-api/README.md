# <img src="https://images.mindcloud.co/apps/icons/openpm_1778171674031.png" alt="openpm logo" width="28" height="28"> openpm: Universal API

Search, publish, and manage OpenAPI packages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openpm/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://openpm.ai
- **Vendor API docs:** https://openpm.ai/apis/openpm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Packages](actions/list-packages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openpm/latest/actions/list-packages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Ai Plugin

| Action | Method | Description |
| --- | --- | --- |
| [Get Package AI Plugin Manifest](actions/get-package-ai-plugin-manifest.md) | GET |  |

### Openapi Spec

| Action | Method | Description |
| --- | --- | --- |
| [Get Package OpenAPI Spec](actions/get-package-openapi-spec.md) | GET |  |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Create Package](actions/create-package.md) | POST |  |
| [Get Package](actions/get-package.md) | GET |  |
| [List Connected Packages](actions/list-connected-packages.md) | GET |  |
| [List Packages](actions/list-packages.md) | GET |  |
| [Lookup Packages](actions/lookup-packages.md) | GET |  |
| [Search Packages](actions/search-packages.md) | GET |  |
| [Update Package](actions/update-package.md) | PUT |  |


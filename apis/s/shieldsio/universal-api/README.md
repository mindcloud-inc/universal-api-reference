# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-05-01-as-10_1777641598346.png" alt="Shields.io logo" width="28" height="28"> Shields.io: Universal API

Generate static, dynamic, and endpoint-backed badges through the public Shields.io badge image service.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shieldsio/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shields.io/
- **Vendor API docs:** https://shields.io/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Static Badge](actions/generate-static-badge.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shieldsio/latest/actions/generate-static-badge?connectionId=$CONNECTION_ID&badgeContent=build-passing-brightgreen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Badge Image

| Action | Method | Description |
| --- | --- | --- |
| [Generate Dynamic JSON Badge](actions/generate-dynamic-json-badge.md) | GET | Retrieves a badge image from JSON data in Shields.io. |
| [Generate Dynamic Regex Badge](actions/generate-dynamic-regex-badge.md) | GET | Retrieves a badge image from regex-matched text in Shields.io. |
| [Generate Dynamic TOML Badge](actions/generate-dynamic-toml-badge.md) | GET | Retrieves a badge image from TOML data in Shields.io. |
| [Generate Dynamic XML Badge](actions/generate-dynamic-xml-badge.md) | GET | Retrieves a badge image from XML data in Shields.io. |
| [Generate Dynamic YAML Badge](actions/generate-dynamic-yaml-badge.md) | GET | Retrieves a badge image from YAML data in Shields.io. |
| [Generate Endpoint Badge](actions/generate-endpoint-badge.md) | GET | Retrieves a badge image from a JSON endpoint in Shields.io. |
| [Generate Static Badge](actions/generate-static-badge.md) | GET | Retrieves a custom static badge image from Shields.io. |


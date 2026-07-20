# <img src="https://images.mindcloud.co/apps/icons/apiary-logo-source_1775488457184.png" alt="Apiary logo" width="28" height="28"> Apiary: Universal API

Apiary is Oracle's API design and documentation platform. This app wraps the token-backed Apiary management routes and public documentation endpoints that are currently exposed and tenant-verifiable.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/apiary/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://apiary.io
- **Vendor API docs:** https://apiary.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List APIs](actions/list-ap-is.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apiary/latest/actions/list-ap-is?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get API Blueprint Snapshot](actions/get-api-blueprint-snapshot.md) | GET |  |
| [Get API Documentation Snapshot](actions/get-api-documentation-snapshot.md) | GET |  |
| [Get API Summary](actions/get-api-summary.md) | GET |  |
| [List APIs](actions/list-ap-is.md) | GET | Finds APIs in your Apiary account. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Blueprint](actions/fetch-blueprint.md) | GET | Retrieves an API blueprint from Apiary by API name. |
| [Publish Blueprint](actions/publish-blueprint.md) | PUT | Publishes an API blueprint in Apiary. |


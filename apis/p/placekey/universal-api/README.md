# <img src="https://images.mindcloud.co/apps/icons/placekey_1776783284918.png" alt="Placekey logo" width="28" height="28"> Placekey: Universal API

Placekey provides APIs for matching physical locations, addresses, and points of interest to stable Placekey identifiers for deduplication, joining, and location intelligence workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/placekey/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.placekey.io/
- **Vendor API docs:** https://docs.placekey.io/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Placekey](actions/get-placekey.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placekey/latest/actions/get-placekey?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Placekey Batch Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Get Placekeys](actions/get-placekeys.md) | GET | Retrieves Placekeys for multiple locations in Placekey. |

### Placekey Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Get Placekey](actions/get-placekey.md) | GET | Retrieves a Placekey for one location in Placekey. |


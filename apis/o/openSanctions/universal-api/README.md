# <img src="https://images.mindcloud.co/apps/icons/open-sanctions_1777911453483.png" alt="OpenSanctions logo" width="28" height="28"> OpenSanctions: Universal API

OpenSanctions provides sanctions, politically exposed person, and other risk data for screening people, companies, and other entities through a hosted API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openSanctions/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.opensanctions.org/
- **Vendor API docs:** https://api.opensanctions.org/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Entity](actions/get-entity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-entity?connectionId=$CONNECTION_ID&entity_id=Q7747" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Adjacent Entity

| Action | Method | Description |
| --- | --- | --- |
| [List Adjacent Entities](actions/list-adjacent-entities.md) | GET |  |
| [List Adjacent Entities By Property](actions/list-adjacent-entities-by-property.md) | GET |  |

### Algorithm

| Action | Method | Description |
| --- | --- | --- |
| [List Matching Algorithms](actions/list-matching-algorithms.md) | GET |  |

### Catalog

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Catalog](actions/get-data-catalog.md) | GET |  |

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [Get Entity](actions/get-entity.md) | GET |  |
| [Search Entities](actions/search-entities.md) | GET |  |

### Entity Match

| Action | Method | Description |
| --- | --- | --- |
| [Match Entity By Example](actions/match-entity-by-example.md) | GET |  |

### Reconciliation

| Action | Method | Description |
| --- | --- | --- |
| [Get Reconciliation Manifest](actions/get-reconciliation-manifest.md) | GET |  |

### Statement

| Action | Method | Description |
| --- | --- | --- |
| [List Entity Statements](actions/list-entity-statements.md) | GET |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Check API Health](actions/check-api-health.md) | GET |  |
| [Check Search Index Readiness](actions/check-search-index-readiness.md) | GET |  |


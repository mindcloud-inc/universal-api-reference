# <img src="https://images.mindcloud.co/apps/icons/interzoid_1776441337228.png" alt="Interzoid logo" width="28" height="28"> Interzoid: Universal API

Interzoid provides AI-powered cloud APIs for data quality, matching, normalization, and enrichment.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/interzoid/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.interzoid.com/
- **Vendor API docs:** https://docs.interzoid.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Remaining Credits](actions/get-remaining-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/get-remaining-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Business Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Business Info](actions/get-business-info.md) | GET |  |

### Company And Address Match Similarity Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Company And Address Match Similarity Key](actions/get-company-and-address-match-similarity-key.md) | GET |  |

### Company And Full Name Match Similarity Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Company And Full Name Match Similarity Key](actions/get-company-and-full-name-match-similarity-key.md) | GET |  |

### Company Match Similarity Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Match Similarity Key](actions/get-company-match-similarity-key.md) | GET |  |

### Full Name And Address Match Similarity Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Full Name And Address Match Similarity Key](actions/get-full-name-and-address-match-similarity-key.md) | GET |  |

### Full Name Match Score

| Action | Method | Description |
| --- | --- | --- |
| [Compare Full Names](actions/compare-full-names.md) | GET |  |

### Full Name Match Similarity Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Full Name Match Similarity Key](actions/get-full-name-match-similarity-key.md) | GET |  |

### Global Address Match Similarity Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Global Address Match Similarity Key](actions/get-global-address-match-similarity-key.md) | GET |  |

### Organization Match Score

| Action | Method | Description |
| --- | --- | --- |
| [Compare Organization Names](actions/compare-organization-names.md) | GET |  |

### Remaining Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Remaining Credits](actions/get-remaining-credits.md) | GET |  |

### Street Address Match Similarity Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Street Address Match Similarity Key](actions/get-street-address-match-similarity-key.md) | GET |  |


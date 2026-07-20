# <img src="https://images.mindcloud.co/apps/icons/w3w-symbol-rgb-red-1_1777582168517.png" alt="What3Words logo" width="28" height="28"> What3Words: Universal API

Convert between what3words addresses and geographic coordinates, suggest valid three-word addresses, inspect grid sections, and list supported address languages.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/what3Words/latest
- **Category:** Support / Field Service
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://what3words.com
- **Vendor API docs:** https://developer.what3words.com/public-api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Available what3words Languages](actions/list-available-what3words-languages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/list-available-what3words-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Grid Section

| Action | Method | Description |
| --- | --- | --- |
| [Get what3words Grid Section](actions/get-what3words-grid-section.md) | GET | Retrieves a what3words grid section by bounding box. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Available what3words Languages](actions/list-available-what3words-languages.md) | GET | Lists available what3words languages for 3 word addresses. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Convert what3words Address to Coordinates](actions/convert-what3words-address-to-coordinates.md) | GET | Retrieves coordinates from a what3words address. |

### What3words Address

| Action | Method | Description |
| --- | --- | --- |
| [Convert Coordinates to what3words Address](actions/convert-coordinates-to-what3words-address.md) | GET | Retrieves a what3words address from coordinates. |

### What3words Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Suggest what3words Addresses](actions/suggest-what3words-addresses.md) | GET | Finds suggested what3words addresses from text input. |


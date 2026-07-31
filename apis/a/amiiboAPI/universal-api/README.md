# <img src="https://images.mindcloud.co/apps/icons/amiibo_1785427013862.png" alt="Amiibo API logo" width="28" height="28"> Amiibo API: Universal API

Browse archived AmiiboAPI catalog and metadata. Provider host is currently unavailable; retest before use.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/amiiboAPI/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://github.com/N3evin/AmiiboAPI
- **Vendor API docs:** https://github.com/N3evin/AmiiboAPI

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Amiibo by ID](actions/get-amiibo-by-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amiiboAPI/latest/actions/get-amiibo-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Amiibo

| Action | Method | Description |
| --- | --- | --- |
| [Get Amiibo by ID](actions/get-amiibo-by-id.md) | GET |  |
| [Get Detailed Amiibo by Head and Tail](actions/get-detailed-amiibo-by-head-and-tail.md) | GET |  |
| [Search Amiibo](actions/search-amiibo.md) | GET |  |

### Amiibo Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Amiibo Series by Key](actions/get-amiibo-series-by-key.md) | GET |  |
| [List Amiibo Series](actions/list-amiibo-series.md) | GET |  |

### Amiibo Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Amiibo Type by Key](actions/get-amiibo-type-by-key.md) | GET |  |
| [List Amiibo Type](actions/list-amiibo-type.md) | GET |  |

### Amiibo Update

| Action | Method | Description |
| --- | --- | --- |
| [Get Amiibo Last Updated](actions/get-amiibo-last-updated.md) | GET |  |

### Character

| Action | Method | Description |
| --- | --- | --- |
| [Get Character by Key](actions/get-character-by-key.md) | GET |  |
| [List Character](actions/list-character.md) | GET |  |

### Game Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Game Series by Key](actions/get-game-series-by-key.md) | GET |  |
| [List Game Series](actions/list-game-series.md) | GET |  |


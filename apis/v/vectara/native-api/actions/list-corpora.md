# List Corpora with Vectara

Retrieves a list of corpora from Vectara.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/corpora`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [List Corpora](https://docs.vectara.com/docs/rest-api/list-corpora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Filter corpora by name or summary. |
| `corpus_id` | query | `string<string>` | no | Limit results to the specified corpus IDs. |
| `page_key` | query | `string` | no | Return the next page of corpora. |

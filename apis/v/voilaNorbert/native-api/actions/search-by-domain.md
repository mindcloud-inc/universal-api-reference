# Search By Domain with VoilaNorbert

Finds contacts in VoilaNorbert by domain or company name.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/domain`
- **Base URL:** `https://api.voilanorbert.com/2018-01-08`
- **Official documentation:** [Search By Domain](https://api.voilanorbert.com/2018-01-08/#search-endpoint-post-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | The company name to search when a domain is not provided. |
| `domain` | body | `string` | no | The company domain to search. |
| `list_id` | body | `number` | no | An optional list id where the found contacts will be attached. |
| `page` | body | `number` | no | The result page to retrieve. |

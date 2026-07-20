# Search By Name with VoilaNorbert

Finds a contact in VoilaNorbert by full name and domain.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/name`
- **Base URL:** `https://api.voilanorbert.com/2018-01-08`
- **Official documentation:** [Search By Name](https://api.voilanorbert.com/2018-01-08/#search-endpoint-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | no | Company domain for the search. |
| `name` | body | `string` | no | Full name of the person to search. |

# Search PACER Cases by Case Title or Party Name with Court Drive

## Endpoint

- **Method:** `GET`
- **Path:** `/cases/pacer/search/party_title`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Search PACER Cases by Case Title or Party Name](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_terms` | query | `string` | yes | Case title or party-name search terms. |

# List Connected Websites with Crisp

Retrieves connected websites from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/plugin/connect/websites/all/:page_number`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [List Connected Websites](https://docs.crisp.chat/references/rest-api/v1/#list-all-connect-websites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_number` | path | `number` | no | The page number for website paging. |
| `filter_configured` | query | `boolean` | no | Restrict to configured plugins only (1 or 0). |
| `include_plan` | query | `boolean` | no | Include the website plan subscription in the response (1 or 0). |

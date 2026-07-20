# List Visitors with Crisp

Retrieves visitors from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/visitors/list/:page_number`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [List Visitors](https://docs.crisp.chat/references/rest-api/v1/#list-visitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier. |
| `page_number` | path | `number` | no | Page number for visitors paging. |

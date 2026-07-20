# Get Accounting Code Details with Kiwili

Retrieves details for an accounting code in Kiwili.

## Endpoint

- **Method:** `GET`
- **Path:** `/accountingcode/:accounting_code_id`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Get Accounting Code Details](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accounting_code_id` | path | `string` | yes | The Kiwili accounting code ID. Use the string 0 for the default record when needed. |

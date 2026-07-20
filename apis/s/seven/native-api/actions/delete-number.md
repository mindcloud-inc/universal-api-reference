# Delete Number with Seven

Deletes an active number from Seven.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/numbers/active/:number`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Delete Number](https://docs.seven.io/en/rest-api/endpoints/numbers#delete-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | path | `string` | yes | The phone number to delete. |
| `delete_immediately` | body | `boolean` | no | If set to true , the number will be deleted immediately. If set to false , the number will be deleted at the end of the current billing period. |

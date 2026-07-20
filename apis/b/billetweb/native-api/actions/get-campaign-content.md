# Get Campaign Content with Billetweb

Retrieves campaign content from your Billetweb account.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaign/:id/data`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [Get Campaign Content](https://www.billetweb.fr/bo/api.php#/api/campaigns/:id/data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Target campaign identifier. |
| `filter` | query | `string` | no | Filter on a specific campaign key. |

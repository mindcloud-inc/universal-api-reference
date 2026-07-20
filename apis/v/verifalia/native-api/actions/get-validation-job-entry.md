# Get Validation Job Entry with Verifalia

Retrieves an entry from an email validation job in Verifalia.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-validations/{id}/entries/{index}`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [Get Validation Job Entry](https://verifalia.com/developers/email-verifications/retrieving-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Verifalia validation job ID. |
| `index` | path | `number` | yes | The zero-based index of the validation entry to retrieve. |

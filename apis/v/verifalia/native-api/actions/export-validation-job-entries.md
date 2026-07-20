# Export Validation Job Entries with Verifalia

Retrieves exported email validation entries from Verifalia.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-validations/{id}/entries`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [Export Validation Job Entries](https://verifalia.com/developers/email-verifications/retrieving-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Verifalia validation job ID. |

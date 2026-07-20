# List Validation Job Entries with Verifalia

Retrieves entries from an email validation job in Verifalia.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-validations/{id}/entries`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [List Validation Job Entries](https://verifalia.com/developers/email-verifications/retrieving-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Verifalia validation job ID. |

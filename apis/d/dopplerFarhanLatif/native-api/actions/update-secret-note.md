# Update Secret Note with Doppler Farhan Latif

Updates a secret note in Doppler.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/projects/project/note`
- **Base URL:** `https://api.doppler.com`
- **Official documentation:** [Update Secret Note](https://docs.doppler.com/reference/secrets-update_note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | Unique identifier for the project object. |
| `secret` | body | `string` | yes | The name of the secret. |
| `note` | body | `string` | yes | The note to set on the secret across environments. |

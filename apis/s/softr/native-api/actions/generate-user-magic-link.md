# Generate User Magic Link with Softr

## Endpoint

- **Method:** `POST`
- **Path:** `https://studio-api.softr.io/v1/api/users/magic-link/generate/:email`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Generate User Magic Link](https://docs.softr.io/softr-api/api-setup-and-endpoints#generate-a-magic-link-for-the-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Email address of the Softr user who needs a magic link. |

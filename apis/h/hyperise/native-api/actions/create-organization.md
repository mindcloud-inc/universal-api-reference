# Create Organization with Hyperise

Creates a client organization in Hyperise.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations`
- **Base URL:** `https://app.hyperise.io/api/v1/regular`
- **Official documentation:** [Create Organization](https://hyperise.customerly.help/en/articles/10000-create-client-account-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The invite email for the client organization. |
| `name` | body | `string` | yes | The client organization name. |
| `seats` | body | `number` | yes | The number of seats to allocate to the client organization. |

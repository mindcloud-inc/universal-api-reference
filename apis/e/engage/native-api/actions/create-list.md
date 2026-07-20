# Create List with Engage

Creates a new list in Engage.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Create List](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#create-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `double_optin` | body | `boolean` | no | Set to true to send a confirmation email to subscribers. |
| `redirect_url` | body | `string` | no | URL to redirect users to after subscription. |
| `title` | body | `string` | yes | List title. |
| `description` | body | `string` | no | List description. |

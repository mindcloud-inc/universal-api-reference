# Create User with Softr

## Endpoint

- **Method:** `POST`
- **Path:** `https://studio-api.softr.io/v1/api/users`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Create User](https://docs.softr.io/softr-api/api-setup-and-endpoints#create-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `full_name` | body | `string` | yes | Full name for the Softr user. |
| `email` | body | `string` | yes | Email address for the Softr user. |
| `password` | body | `string` | no | Password for the Softr user. Leave blank to let Softr generate one automatically. |
| `generate_magic_link` | body | `boolean` | no | Whether Softr should generate a magic link for the new user. |

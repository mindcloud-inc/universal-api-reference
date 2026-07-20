# Resolve Person From Email with Reverse Contact

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/resolve/persons/email`
- **Base URL:** `https://api.reversecontact.com`
- **Official documentation:** [Resolve Person From Email](https://app.reversecontact.com/docs/endpoints/resolve-person-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to resolve. |
| `webhookUrl` | body | `string` | no | HTTPS callback URL for async results. |

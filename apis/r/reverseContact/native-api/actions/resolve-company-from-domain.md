# Resolve Company From Domain with Reverse Contact

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/resolve/companies/live`
- **Base URL:** `https://api.reversecontact.com`
- **Official documentation:** [Resolve Company From Domain](https://app.reversecontact.com/docs/endpoints/resolve-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Company domain to resolve. |
| `webhookUrl` | body | `string` | no | HTTPS callback URL for async results. |

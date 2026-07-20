# Create API Key with Snappy

Creates a new API key in Snappy.

## Endpoint

- **Method:** `POST`
- **Path:** `/authentication/apiKeys`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Create API Key](https://docs.snappy.com/reference/createapikey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the API key. |
| `expirationInDays` | body | `number` | no | API key expiration period in days. |
| `enforceMtls` | body | `boolean` | no | Whether to enforce mTLS for the API key. |
| `permissions[]` | body | `array<string>` | no | Permissions granted to the API key. |
| `companyId` | query | `string` | no | Company ID. |

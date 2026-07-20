# Create Vonage provider with Appwrite

Creates a new vonage provider in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/providers/vonage`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create Vonage provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | body | `string` | yes | Provider ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | body | `string` | yes | Provider name. |
| `from` | body | `string` | no | Sender Phone number. Format this number with a leading '+' and a country code, e.g., +16175551212. |
| `apiKey` | body | `string` | no | Vonage API key. |
| `apiSecret` | body | `string` | no | Vonage API secret. |
| `enabled` | body | `boolean` | no | Set as enabled. |

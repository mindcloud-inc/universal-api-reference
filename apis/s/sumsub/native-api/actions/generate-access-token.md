# Generate Access Token with Sumsub

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/accessTokens/sdk`
- **Base URL:** `https://api.sumsub.com`
- **Official documentation:** [Generate Access Token](https://docs.sumsub.com/reference/generate-access-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ttlInSecs` | body | `number` | no | Token lifespan in seconds. Sumsub defaults this value to 600 when omitted. |
| `userId` | body | `string` | yes | Applicant identifier on your side. |
| `levelName` | body | `string` | yes | Verification level used for the SDK token. |

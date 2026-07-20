# Verify Email (MORE V3 BSON) with Email Hippo

Verifies an email address with Email Hippo MORE V3 BSON.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/more/bson/{apiKey}/:emailAddress`
- **Base URL:** `https://api.hippoapi.com`
- **Official documentation:** [Verify Email (MORE V3 BSON)](https://docs.emailhippo.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/bson` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | path | `string` | yes | The email address to verify. |

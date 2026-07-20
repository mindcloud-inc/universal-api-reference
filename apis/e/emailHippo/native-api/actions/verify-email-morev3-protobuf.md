# Verify Email (MORE V3 Protobuf) with Email Hippo

Verifies an email address with Email Hippo MORE V3 Protobuf.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/more/proto/{apiKey}/:emailAddress`
- **Base URL:** `https://api.hippoapi.com`
- **Official documentation:** [Verify Email (MORE V3 Protobuf)](https://docs.emailhippo.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/x-protobuf` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | path | `string` | yes | The email address to verify. |

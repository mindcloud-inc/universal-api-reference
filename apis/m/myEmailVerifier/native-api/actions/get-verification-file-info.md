# Get Verification File Info with MyEmailVerifier

Retrieves bulk verification job details from MyEmailVerifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/verifier/file_info/{apiKey}/:fileId`
- **Base URL:** `https://client.myemailverifier.com`
- **Official documentation:** [Get Verification File Info](https://myemailverifier.com/real-time-email-verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `number` | yes | Bulk verification file ID returned by Upload Verification File. |

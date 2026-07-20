# Validate Email Batch with ZeroBounce

Finds email validation results in ZeroBounce by batch request.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/validatebatch`
- **Base URL:** `https://api.zerobounce.net`
- **Official documentation:** [Validate Email Batch](https://www.zerobounce.net/docs/email-validation-api-quickstart/v2-batch-validate-emails)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_batch[]` | body | `array<object>` | yes | — |
| `email_batch[].email_address` | body | `string` | yes | Email address for one batch validation item. |
| `timeout` | body | `number` | no | — |
| `activity_data` | body | `boolean` | no | — |
| `verify_plus` | body | `boolean` | no | — |

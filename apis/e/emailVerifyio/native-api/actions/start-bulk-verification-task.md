# Start Bulk Verification Task with EmailVerify.io

Creates a bulk verification task in EmailVerify.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate-batch`
- **Base URL:** `https://app.emailverify.io/api/v1`
- **Official documentation:** [Start Bulk Verification Task](https://www.emailverify.io/api/docs/#bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title for the bulk verification task. |
| `email_batch` | body | `object` | yes | Array of email-address objects to verify in bulk. Send multiple values as a array. |

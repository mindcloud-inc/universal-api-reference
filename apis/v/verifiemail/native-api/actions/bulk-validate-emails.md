# Bulk Validate Emails with verifi.email

Retrieves bulk email validation results from verifi.email using a JSON array.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/bulk/check`
- **Base URL:** `https://api.verifi.email`
- **Official documentation:** [Bulk Validate Emails](https://verifi.email/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | query | `string` | yes | Comma-separated email addresses to validate. |

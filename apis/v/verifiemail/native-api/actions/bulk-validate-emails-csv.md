# Bulk Validate Emails CSV with verifi.email

Retrieves bulk email validation results from verifi.email using the emails query parameter.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/bulk/check`
- **Base URL:** `https://api.verifi.email`
- **Official documentation:** [Bulk Validate Emails CSV](https://verifi.email/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | query | `string` | yes | Comma-separated email addresses to validate. |

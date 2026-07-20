# Create Dashboard Email with Boomlify

Creates a new dashboard email in Boomlify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/emails/create`
- **Base URL:** `https://v1.boomlify.com`
- **Official documentation:** [Create Dashboard Email](https://boomlify.com/en/temp-mail-api-docs?endpoint=create-dashboard-email&tab=docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_username` | query | `string` | no | Optional custom local-part for the dashboard email address. |
| `domain` | query | `string` | no | Optional custom domain for the dashboard email address. |

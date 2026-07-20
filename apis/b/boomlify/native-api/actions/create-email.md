# Create Email with Boomlify

Creates a new temporary email address in Boomlify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/emails/create`
- **Base URL:** `https://v1.boomlify.com`
- **Official documentation:** [Create Email](https://boomlify.com/en/temp-mail-api-docs?endpoint=create-email&tab=docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_username` | query | `string` | no | Optional custom local-part for the generated temporary email address. |
| `time` | query | `list` | no | Optional email duration. Documented values are 10min, 1hour, 1day, and permanent. Accepted values: `0`, `1`, `2`, `3`. |
| `domain` | query | `string` | no | Optional custom domain for the generated email address. |
| `create_as_dashboard` | query | `boolean` | no | Whether to create the address as a dashboard email. |

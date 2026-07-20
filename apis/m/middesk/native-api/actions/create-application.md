# Create an application with Middesk

Creates an application in your Middesk account.

## Endpoint

- **Method:** `POST`
- **Path:** `/partner/applications`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create an application](https://docs.middesk.com/docs/jurisdiction-registration-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | body | `string` | yes | Existing Middesk company ID for the application. |

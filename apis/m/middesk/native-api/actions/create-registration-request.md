# Create a registration request with Middesk

Creates a registration request in Middesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/partner/registration_requests`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create a registration request](https://docs.middesk.com/docs/jurisdiction-registration-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | body | `string` | yes | Existing Middesk company ID to associate with the registration request. |
| `company_name` | body | `string` | no | Company name used to create the registration request when no company ID is provided. |
| `email` | body | `string` | yes | Email address of the applicant or contact. |
| `state` | body | `string` | yes | US state where the registration request is being created. |

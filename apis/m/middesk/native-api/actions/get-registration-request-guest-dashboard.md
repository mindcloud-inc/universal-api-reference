# Fetch guest dashboard link for a registration request with Middesk

Retrieves a guest dashboard link from Middesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/partner/registration_requests/:id/guest_dashboard`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Fetch guest dashboard link for a registration request](https://docs.middesk.com/docs/jurisdiction-registration-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the registration request whose guest dashboard you want to fetch. |

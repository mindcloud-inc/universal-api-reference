# Submit Routing Form with Calendly

Submits a routing form in Calendly.

## Endpoint

- **Method:** `POST`
- **Path:** `/routing_forms/submit`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Submit Routing Form](https://developer.calendly.com/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form` | body | `string` | yes | Routing form URI. |
| `responses` | body | `list<string>` | yes | Routing form response payload. |

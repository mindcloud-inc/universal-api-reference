# Create Partner with Trak Qr Automation

Creates a new partner in Trak Qr Automation.

## Endpoint

- **Method:** `POST`
- **Path:** `/events-partners`
- **Base URL:** `https://backend.trak.codes/api/v0`
- **Official documentation:** [Create Partner](https://docs.google.com/document/u/2/d/e/2PACX-1vSFebcwRE1ntGhoYLQB90Ujf5BfUFocWmZWTfw1FGW3LawP3Q7ZDDOGwHEwsVQnwXJO2tdj1d8NQqit/pub?urp=gmail_link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Contact email where the Trak API key will be sent. |
| `brand` | body | `string` | yes | User-facing brand name of your product. |
| `description` | body | `string` | yes | Description of your integration use case. This is not shown to users. |

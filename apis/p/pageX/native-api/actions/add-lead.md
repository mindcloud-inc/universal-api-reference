# Add Lead with PageX

## Endpoint

- **Method:** `POST`
- **Path:** `/api/lead`
- **Base URL:** `https://www.pagexcrm.com`
- **Official documentation:** [Add Lead](https://rapidapi.com/thunderhurt/api/pagexcrm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Full name of the lead. |
| `email` | body | `string` | no | Email address of the lead. |
| `phone` | body | `string` | no | Phone number of the lead. |
| `plat` | body | `string` | no | Lead source platform, such as facebook, insta, or x. |
| `customer_id` | body | `string` | no | Customer identifier when the source system already has one. |

# Create Redirect with redirect.pizza

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/redirects`
- **Base URL:** `https://redirect.pizza`
- **Official documentation:** [Create Redirect](https://redirect.pizza/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sources[]` | body | `array<string>` | yes | URLs to redirect from. |
| `destination` | body | `string` | yes | Destination URL for the redirect. |
| `redirect_type` | body | `string` | yes | Redirect mode such as permanent or temporary. |
| `uri_forwarding` | body | `boolean` | no | Whether to forward the request path. |
| `keep_query_string` | body | `boolean` | no | Whether to forward the query string. |
| `tracking` | body | `boolean` | no | Whether to collect analytics for the redirect. |
| `tags[]` | body | `array<string>` | no | Tags that categorize the redirect. |
| `notes` | body | `string` | no | Internal notes about the redirect. |
| `merge` | body | `boolean` | no | Merge into an existing redirect with the same destination when possible. |
| `upsert` | body | `boolean` | no | Update an existing redirect when a provided source already exists. |

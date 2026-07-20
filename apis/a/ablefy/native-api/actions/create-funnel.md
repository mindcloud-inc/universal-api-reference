# Create Funnel with Ablefy

Creates a new funnel in Ablefy.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/funnels`
- **Base URL:** `https://api.myablefy.com`
- **Official documentation:** [Create Funnel](https://api.myablefy.com/api/swagger_doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `funnel_node_attributes.content_page_id` | body | `string` | no | Required content_page_id |
| `funnel_node_attributes.form` | body | `list<string>` | no | Funnel node form Accepted values: `node_link`, `node_page`. |
| `funnel_node_attributes.redirection_url` | body | `string` | no | Redirection url if type is link |
| `name` | body | `string` | no | — |
| `funnel_node_attributes` | body | `object` | yes | — |

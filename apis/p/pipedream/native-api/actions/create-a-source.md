# Create a source with Pipedream

Creates a new source in Pipedream.

## Endpoint

- **Method:** `POST`
- **Path:** `/sources`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Create a source](https://pipedream.com/docs/rest-api/api-reference/sources/create-a-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component_code` | body | `string` | no | The full Pipedream component code. |
| `component_id` | body | `string` | no | The ID of a component already created in your account. |
| `component_url` | body | `string` | no | A URL reference to the hosted component source. |
| `name` | body | `string` | no | Optional source name. Defaults to the component name slug when omitted. |

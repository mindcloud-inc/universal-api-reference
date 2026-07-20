# Create a component with Pipedream

Creates a new component in Pipedream.

## Endpoint

- **Method:** `POST`
- **Path:** `/components`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Create a component](https://pipedream.com/docs/rest-api/api-reference/components/create-a-component)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component_code` | body | `string` | no | The full Pipedream component code. |
| `component_url` | body | `string` | no | A URL reference to the hosted component source. |

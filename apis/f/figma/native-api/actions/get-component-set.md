# Get Component Set with Figma

Retrieves a component set from Figma by key.

## Endpoint

- **Method:** `GET`
- **Path:** `/component_sets/:key`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Get Component Set](https://developers.figma.com/docs/rest-api/component-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | The unique key of the component set. |

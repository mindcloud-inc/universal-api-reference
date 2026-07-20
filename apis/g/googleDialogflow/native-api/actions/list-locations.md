# List Locations with Google Dialogflow

Retrieves locations from Google Dialogflow.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/:name/locations`
- **Base URL:** `https://dialogflow.googleapis.com`
- **Official documentation:** [List Locations](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Google Cloud project resource name, for example projects/my-project. |
| `filter` | query | `string` | no | Optional Google locations filter expression. |
| `extraLocationTypes[]` | query | `array<string>` | no | Optional extra Google Cloud location types to include. Send multiple values as a array. |

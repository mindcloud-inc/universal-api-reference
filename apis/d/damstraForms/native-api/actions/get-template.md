# Get Template with Damstra Forms

Retrieves a template from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Template](https://sammapi.docs.apiary.io/#reference/templates/template-instance/retrieve-a-template)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The unique identifier of the template. |
| `show_managed` | query | `boolean` | no | Determines whether to include integrated templates in the response. |

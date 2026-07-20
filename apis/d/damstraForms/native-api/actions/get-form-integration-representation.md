# Get Form Integration Representation with Damstra Forms

Retrieves a form in integration format from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Form Integration Representation](https://sammapi.docs.apiary.io/#reference/forms/form-instance/retrieve-a-form)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The unique identifier of the form. |
| `representation` | query | `string` | no | If "integration" is specified will display the form using integration tags |
| `include_children` | query | `boolean` | no | If true the metadata section will include information about any linked child forms or actions |

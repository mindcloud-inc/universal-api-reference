# List Integration Property Group Properties with Ziflow

Retrieves integration property group properties from Ziflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/integrations/:applicationKey/property-groups/:key/properties`
- **Base URL:** `https://api.ziflow.io/v1`
- **Official documentation:** [List Integration Property Group Properties](https://api-docs.ziflow.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `application_key` | path | `string` | yes | Integration application key. |
| `key` | path | `string` | yes | Integration property group key. |

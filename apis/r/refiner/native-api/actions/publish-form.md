# Publish Form with Refiner

Publishes or unpublishes a form in Refiner.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/publish`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [Publish Form](https://refiner.io/docs/api/#publish-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_uuid` | body | `string` | yes | The form UUID to publish or unpublish. |
| `published` | body | `boolean` | no | Set to false to unpublish the form. |

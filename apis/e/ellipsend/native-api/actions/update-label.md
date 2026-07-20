# Update Label with Ellipsend

Updates an existing label in Ellipsend.

## Endpoint

- **Method:** `PUT`
- **Path:** `/label/[:label_id]`
- **Base URL:** `https://api.ellipsend.com/v1`
- **Official documentation:** [Update Label](https://api.ellipsend.com/v1/docs#/Label/put_label__label_id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label_id` | path | `number` | yes | The label ID. |
| `label` | body | `string` | yes | The new label value. |

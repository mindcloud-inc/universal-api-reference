# Add a Class with DocuPanda - Document Understanding

Creates a new class in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/class`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Add a Class](https://docs.docupipe.ai/reference/post_add_class)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `className` | body | `string` | yes | Name of the class to be added. |
| `description` | body | `string` | no | Description of the class to be added. This will be used by the AI to classify documents. |

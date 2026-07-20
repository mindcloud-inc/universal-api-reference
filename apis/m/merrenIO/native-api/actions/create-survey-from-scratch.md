# Create Survey From Scratch with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/survey/create`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Create Survey From Scratch](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.name` | body | `string` | yes | Name of the new survey. |
| `input.category` | body | `string` | yes | Survey category label, such as Other or Customer Satisfaction. |
| `input.created_by` | body | `string` | yes | Creator email used by Merren when creating the survey. |
| `input.description` | body | `string` | no | Optional survey description. |

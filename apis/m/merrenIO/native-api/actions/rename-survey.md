# Rename Survey with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/survey/update`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Rename Survey](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey to rename. |
| `name` | body | `string` | yes | New survey name. |

# Change Survey Category with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/survey/update`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Change Survey Category](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey to update. |
| `category` | body | `string` | yes | New survey category. |

# Add Survey Language Set with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/survey/update`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Add Survey Language Set](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey to update. |
| `languages` | body | `string` | yes | Language labels to add to the survey. |

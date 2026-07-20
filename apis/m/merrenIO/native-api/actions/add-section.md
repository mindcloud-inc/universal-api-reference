# Add Section with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/section/save`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Add Section](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.title` | body | `string` | yes | Title of the section. |
| `input.surveyId` | body | `string` | yes | Survey that will own the section. |

# Retrieve Question Responses with Drag'n Survey

Retrieves responses for a Drag'n Survey question.

## Endpoint

- **Method:** `GET`
- **Path:** `components/:componentId/responses`
- **Base URL:** `https://developer.dragnsurvey.com/api/v2.0.0`
- **Official documentation:** [Retrieve Question Responses](https://developer.dragnsurvey.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `componentId` | path | `string` | no | The Drag'n Survey component ID. |
| `reportId` | query | `string` | no | Limit component responses to the report filter. |

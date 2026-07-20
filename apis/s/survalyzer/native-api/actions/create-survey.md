# Create Survey with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Survey/v3/CreateSurvey`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [Create Survey](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | body | `number` | yes |
| `name` | body | `string` | yes |
| `surveyDefinition` | body | `object` | yes |
| `surveyConfiguration` | body | `object` | no |

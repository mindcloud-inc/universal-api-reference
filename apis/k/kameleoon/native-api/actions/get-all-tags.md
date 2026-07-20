# Get all tags with Kameleoon

## Endpoint

- **Method:** `GET`
- **Path:** `tags`
- **Base URL:** `https://api.kameleoon.com`
- **Official documentation:** [Get all tags](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-tags/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paramsIO` | query | `string` | yes | Required query object documented by Kameleoon for list endpoints. |
| `type` | query | `string` | yes | Tag type filter required by Kameleoon tags endpoint. Valid values include EXPERIMENT, FEATURE, PERSONALIZATION, SEGMENT, GOAL, WIDGET, STUDIO_THEME, TEAM, IMAGE, AI_EXPLORATION_SCOPE, KEY_MOMENT. |

# Get Keyword Suggestions with AppFollow

Retrieves keyword suggestions from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/aso/suggests`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [Get Keyword Suggestions](https://docs.api.appfollow.io/reference/aso_keyword_research_api_v2_aso_suggests_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | Search term. |
| `country` | query | `string` | no | Country code. |
| `device` | query | `string` | no | Device type. |

# Get All Templates For App with Gupshup

Retrieves all templates for a Gupshup app.

## Endpoint

- **Method:** `GET`
- **Path:** `/wa/app/{app_id}/template`
- **Base URL:** `https://api.gupshup.io`
- **Official documentation:** [Get All Templates For App](https://docs.gupshup.io/reference/get-all-templates-for-an-app)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | Gupshup app ID. |
| `languageCode` | query | `string` | no | Filter templates by language code. |
| `quality` | query | `string` | no | Filter templates by quality rating. |
| `templateCategory` | query | `string` | no | Filter templates by category: marketing, utility, or authentication. |
| `templateStatus` | query | `string` | no | Filter templates by status, for example APPROVED. |
| `templateType` | query | `string` | no | Filter templates by template type. |
| `pageNo` | query | `number` | no | Page number for paginated template results. |
| `pageSize` | query | `number` | no | Number of templates per page. |

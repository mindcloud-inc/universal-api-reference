# Create Badge with IssueBadge

## Endpoint

- **Method:** `POST`
- **Path:** `/badge/create`
- **Base URL:** `https://app.issuebadge.com/api/v1`
- **Official documentation:** [Create Badge](https://app.issuebadge.com/docs/api-documentation.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Badge name Maximum length: 200. |
| `description` | body | `string` | yes | Badge description |
| `badge_logo` | body | `file` | yes | Badge logo image file |
| `issuing_organization_name` | body | `string` | yes | Name of the issuing organization Maximum length: 200. |
| `idempotency_key` | body | `string` | yes | Unique key to prevent duplicate badge creation Maximum length: 80. |
| `nickname` | body | `string` | no | Optional badge nickname |
| `left_panel_description` | body | `string` | no | Additional description for the left panel |
| `organization_id` | body | `string` | no | Existing organization ID |
| `comment` | body | `string` | no | Additional comments Maximum length: 200. |
| `expire_date` | body | `date` | no | Badge expiration date |
| `custom_fields[]` | body | `array<object>` | no | Custom fields for this badge |

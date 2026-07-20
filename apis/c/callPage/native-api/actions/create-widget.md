# Create Widget with CallPage

Creates a new widget in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/widgets/create`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Create Widget](https://callpage.github.io/documentation-rest/#create-widget)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `url` | body | `string` | yes |
| `description` | body | `string` | no |
| `locale_code` | body | `string` | no |

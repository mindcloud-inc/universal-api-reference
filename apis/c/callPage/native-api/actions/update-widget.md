# Update Widget with CallPage

Updates an existing widget in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/widgets/update`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Update Widget](https://callpage.github.io/documentation-rest/#update-widget)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | yes |
| `url` | body | `string` | yes |
| `description` | body | `string` | no |
| `settings` | body | `list<object>` | no |
| `locale_code` | body | `string` | no |
| `enabled` | body | `boolean` | no |

# Update Template with OneSignal

Updates an existing template in OneSignal.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/templates/:template_id`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Update Template](https://documentation.onesignal.com/reference/update-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contents` | body | `object` | no | Localized template contents keyed by language code. |
| `name` | body | `string` | no | An updated name for the template. |
| `template_id` | path | `string` | yes | The identifier of the template in UUID v4 format. |

# Create Template with OneSignal

Creates a template in OneSignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Create Template](https://documentation.onesignal.com/reference/create-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contents` | body | `object` | yes | Localized template contents keyed by language code, such as {"en":"Hello from OneSignal"}. |
| `name` | body | `string` | yes | A name for the template. |

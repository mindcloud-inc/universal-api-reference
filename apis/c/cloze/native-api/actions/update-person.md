# Update Person with Cloze

Updates a person in Cloze.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/update`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Update Person](https://api.cloze.com/api-docs/#/paths/v1-people-update/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `direct` | body | `string` | no | Direct identifier for the person to update. |
| `emails[]` | body | `array<object>` | no | Email addresses for the person. |
| `emails[].value` | body | `string` | no | Email address value. |
| `stage` | body | `list<string>` | no | Stage of the person. Accepted values: `current`, `future`, `lead`, `out`, `past`. |

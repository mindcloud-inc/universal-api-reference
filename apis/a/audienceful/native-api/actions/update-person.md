# Update Person with Audienceful

Updates an existing person in Audienceful.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/people/`
- **Base URL:** `https://app.audienceful.com/api`
- **Official documentation:** [Update Person](https://developer.audienceful.com/api-reference/people/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The person's email. |
| `tags[]` | body | `array<string>` | no | Comma-separated tags. Missing tags are created. |
| `notes` | body | `string` | no | Notes associated with this person. |
| `extra_data` | body | `object` | no | Custom field payload for this person. |

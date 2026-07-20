# Create Person with Audienceful

Creates a new person in Audienceful.

## Endpoint

- **Method:** `POST`
- **Path:** `/people/`
- **Base URL:** `https://app.audienceful.com/api`
- **Official documentation:** [Create Person](https://developer.audienceful.com/api-reference/people/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The person's email. |
| `tags[]` | body | `array<string>` | no | Comma-separated tags. Missing tags are created. |
| `notes` | body | `string` | no | Notes associated with this person. |
| `extra_data` | body | `object` | no | Custom field payload for this person. |
| `double_opt_in` | body | `string` | no | Double opt-in state for the person. |
| `trigger_automations` | body | `boolean` | no | Trigger matching automations when the person is added. |

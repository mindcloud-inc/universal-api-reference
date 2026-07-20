# Update Staff Member with ServiceM8

## Endpoint

- **Method:** `POST`
- **Path:** `/api_1.0/staff/:uuid.json`
- **Base URL:** `https://api.servicem8.com`
- **Official documentation:** [Update Staff Member](https://developer.servicem8.com/reference/updatestaffmembers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | UUID of the Staff Member |
| `first` | body | `string` | yes | Staff First Name |
| `last` | body | `string` | yes | Staff Last Name |
| `email` | body | `string` | yes | Staff Email Address. This is also your login name. |
| `mobile` | body | `string` | no | Mobile phone number of the staff member. Used for SMS communications and identification when calling. |
| `job_title` | body | `string` | no | The staff member's job title or role within the organization. |
| `color` | body | `string` | no | The color assigned to this staff member, represented as a hex color code. |
| `hide_from_schedule` | body | `number` | no | Boolean flag controlling whether this staff member appears in the schedule view. |
| `lng` | body | `number` | no | Longitude coordinate of the staff member's current or last known location. Used for tracking staff locations and calculating routes and travel distances. |
| `lat` | body | `number` | no | Latitude coordinate of the staff member's current or last known location. Used for tracking staff locations and calculating routes and travel distances. |
| `geo_timestamp` | body | `date` | no | The date and time when the staff member's geographic location was last updated. |
| `navigating_to_job_uuid` | body | `string` | no | UUID of the job the staff member is currently navigating to. |
| `navigating_timestamp` | body | `date` | no | The date and time when the staff member started navigating to a job. |
| `navigating_expiry_timestamp` | body | `date` | no | The date and time when navigation to a job is expected to complete or expire. |
| `status_message` | body | `string` | no | Short message summarising the staff's current status. |
| `status_message_timestamp` | body | `date` | no | The date and time when the staff member's status message was last updated. |
| `can_receive_push_notification` | body | `string` | no | Whether the staff member can receive push notifications. |
| `security_role_uuid` | body | `string` | no | Security role UUID. |
| `labour_material_uuid` | body | `string` | no | Labour material UUID. |

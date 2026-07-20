# Add status activity with Status Hero

## Endpoint

- **Method:** `POST`
- **Path:** `/status_activities`
- **Base URL:** `https://service.statushero.com/api/v1`
- **Official documentation:** [Add status activity](https://api.statushero.com/#add-a-status-activity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address for the associated team member. Must match a Status Hero member. |
| `source` | body | `string` | yes | The external activity source name, such as a board or repository. |
| `description` | body | `string` | yes | Brief activity description. Simple HTML markup is accepted by Status Hero. |
| `source_url` | body | `string` | no | Optional external URL for the activity source. |

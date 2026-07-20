# Create Client Project with Audome

## Endpoint

- **Method:** `POST`
- **Path:** `/client-projects`
- **Base URL:** `https://app.audome.com/api/v1`
- **Official documentation:** [Create Client Project](https://app.audome.com/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_name` | body | `string` | yes | Customer display name. |
| `note` | body | `string` | no | Optional project note. |
| `password` | body | `string` | no | Optional project password. |
| `sent_at` | body | `date` | no | Optional sent timestamp. |
| `title` | body | `string` | yes | Project title. |

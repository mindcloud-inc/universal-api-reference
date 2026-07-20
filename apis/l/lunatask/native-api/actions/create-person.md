# Create Person with Lunatask

## Endpoint

- **Method:** `POST`
- **Path:** `/people`
- **Base URL:** `https://api.lunatask.app/v1`
- **Official documentation:** [Create Person](https://lunatask.app/api/people-api/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | A person's first name |
| `last_name` | body | `string` | yes | A person's last name |
| `relationship_strength` | body | `string` | no | Relationship strength classification for the person |
| `source` | body | `string` | no | Identification of the external system where the person is coming from |
| `source_id` | body | `string` | no | The ID of the record in the external system |
| `email` | body | `string` | no | The person's email address |
| `birthday` | body | `date` | no | The person's birthday |
| `phone` | body | `string` | no | The person's phone number |

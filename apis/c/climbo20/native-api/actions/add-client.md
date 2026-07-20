# Add Client with Climbo 2.0

Creates a new client in Climbo 2.0.

## Endpoint

- **Method:** `POST`
- **Path:** `/client`
- **Base URL:** `https://api.climbo.com`
- **Official documentation:** [Add Client](https://climbo.readme.io/reference/add-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_name` | body | `string` | no | Name of the customer. |
| `email` | body | `string` | yes | Email of the customer. |
| `plan_id` | body | `string` | yes | Plan ID to associate to the customer. |
| `welcome` | body | `string` | no | Send welcome email to the customer with a magic link to log in. |
| `password` | body | `string` | no | Must be at least 8 characters. |

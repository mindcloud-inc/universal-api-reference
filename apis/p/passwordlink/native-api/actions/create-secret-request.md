# Create Secret Request with Password.link

## Endpoint

- **Method:** `POST`
- **Path:** `/secret_requests`
- **Base URL:** `https://password.link/api`
- **Official documentation:** [Create Secret Request](https://password.link/en/p/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Description for the Secret Request. |
| `message` | body | `string` | no | Message for the Secret Request viewer. |
| `expiration` | body | `number` | no | Expiration time for the Secret Request, in hours. |
| `limit` | body | `number` | no | Usage limit for the Secret Request. |
| `send_request_to_email` | body | `string` | no | Send the created Secret Request link to the given email address. |
| `send_to_email` | body | `string` | no | Send the created Secret link created using the Secret Request to the given email address. |
| `secret_description` | body | `string` | no | Description for the Secret created using the Secret Request. |
| `secret_message` | body | `string` | no | Message for the Secret created using the Secret Request. |
| `secret_expiration` | body | `number` | no | Expiration time for the Secret created using the Secret Request, in hours. |
| `secret_password` | body | `string` | no | Password for the Secret created using the Secret Request, in hours. |
| `secret_max_views` | body | `number` | no | Maximum views for the Secret created using the Secret Request. |

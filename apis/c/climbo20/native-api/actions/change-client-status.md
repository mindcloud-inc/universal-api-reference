# Change Client Status with Climbo 2.0

Updates a client's status in Climbo 2.0.

## Endpoint

- **Method:** `POST`
- **Path:** `/client/{client_id}/change-status`
- **Base URL:** `https://api.climbo.com`
- **Official documentation:** [Change Client Status](https://climbo.readme.io/reference/change-client-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | ID of your customer. |
| `status` | query | `string` | yes | New customer status. |

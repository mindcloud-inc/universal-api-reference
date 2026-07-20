# Change Client Plan with Climbo 2.0

Updates a client's plan in Climbo 2.0.

## Endpoint

- **Method:** `POST`
- **Path:** `/client/{client_id}/change-plan`
- **Base URL:** `https://api.climbo.com`
- **Official documentation:** [Change Client Plan](https://climbo.readme.io/reference/change-client-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | ID of your customer. |
| `plan_id` | query | `string` | yes | Plan ID to assign to the customer. |

# Ignore Authorization Request with Conveyor

Marks an authorization request as ignored in Conveyor.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/exchange/authorization_requests/:authorization_request_id`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [Ignore Authorization Request](https://docs.conveyor.com/reference/patch-authorization-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorization_request_id` | path | `string` | yes | Authorization request identifier. |
| `reviewer_email` | query | `string` | yes | Reviewer email for the status update. |

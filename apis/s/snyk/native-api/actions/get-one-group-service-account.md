# Get Group Service Account with Snyk

Retrieves a service account from a Snyk group.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_id/service_accounts/:serviceaccount_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get Group Service Account](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceaccount_id` | path | `string` | yes | Snyk service account ID for the request path. |

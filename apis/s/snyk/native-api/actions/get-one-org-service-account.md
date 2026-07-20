# Get Organization Service Account with Snyk

Retrieves a service account from a Snyk organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/service_accounts/:serviceaccount_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get Organization Service Account](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceaccount_id` | path | `string` | yes | Snyk service account ID for the request path. |

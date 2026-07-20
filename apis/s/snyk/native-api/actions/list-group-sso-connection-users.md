# List Group SSO Connection Users with Snyk

Retrieves users from a Snyk group SSO connection.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_id/sso_connections/:sso_id/users`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [List Group SSO Connection Users](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sso_id` | path | `string` | yes | Snyk SSO connection ID for the request path. |

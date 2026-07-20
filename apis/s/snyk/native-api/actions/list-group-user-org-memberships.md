# List Group Organization Memberships with Snyk

Retrieves group organization memberships for a Snyk user.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_id/org_memberships`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [List Group Organization Memberships](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | query | `string` | yes | Snyk user ID for the required query filter. |

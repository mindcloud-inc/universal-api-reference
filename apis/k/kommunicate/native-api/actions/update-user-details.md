# Update User Details with Kommunicate

Updates an existing user in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/user/update`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Update User Details](https://docs.kommunicate.io/docs/api-detail#update-user-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ofUserId` | body | `string` | yes | User ID to route into the required Of-User-Id header. |
| `email` | body | `string` | no | Updated email address for the user. |
| `displayName` | body | `string` | no | Updated display name for the user. |
| `imageLink` | body | `string` | no | Updated profile image URL for the user. |
| `metadata` | body | `object` | no | Optional user metadata fields visible in the dashboard. |

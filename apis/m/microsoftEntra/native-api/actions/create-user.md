# Create User with Microsoft Entra

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Create User](https://learn.microsoft.com/en-us/graph/api/user-post-users?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | yes | — |
| `passwordProfile.password` | body | `string` | yes | — |
| `passwordProfile.forceChangePasswordNextSignIn` | body | `boolean` | no | — |
| `userPrincipalName` | body | `string` | yes | The domain must be a verified domain in your tenant. |
| `mailNickname` | body | `string` | yes | — |
| `accountEnabled` | body | `boolean` | yes | — |
| `passwordProfile` | body | `object` | yes | — |
| `onPremisesImmutableId` | body | `string` | no | Required when the user's sign-in domain is federated. |

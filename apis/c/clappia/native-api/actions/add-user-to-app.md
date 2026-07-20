# Add User to App with Clappia

Creates a new app user membership in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/addUserToApp`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Add User to App](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | body | `string` | no | Email address of the app user to add. |
| `phoneNumber` | body | `string` | no | Phone number of the app user to add. |
| `appId` | body | `string` | yes | Clappia app ID. |
| `permissions` | body | `object` | yes | Permissions object describing the app access to grant. |

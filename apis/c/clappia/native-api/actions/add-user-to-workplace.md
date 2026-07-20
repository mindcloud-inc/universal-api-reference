# Add User to Workplace with Clappia

Creates a new workplace user in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/workplace/addUserToWorkplace`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Add User to Workplace](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | body | `string` | no | Email address of the workplace user to add. |
| `phoneNumber` | body | `string` | no | Phone number of the workplace user to add. |
| `attributes` | body | `object` | no | Optional attribute object to assign when adding the user. |
| `groupNames[]` | body | `array<string>` | no | Optional group names to assign when adding the user. |

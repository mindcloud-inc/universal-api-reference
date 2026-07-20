# Update Workplace User Groups with Clappia

Updates workplace user groups in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/workplace/updateWorkplaceUserGroups`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update Workplace User Groups](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | body | `string` | no | Email address of the workplace user to update. |
| `phoneNumber` | body | `string` | no | Phone number of the workplace user to update. |
| `groupNames[]` | body | `array<string>` | yes | Array of Clappia group names to assign. |

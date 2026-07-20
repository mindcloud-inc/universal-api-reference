# Update Workplace User Role with Clappia

Updates workplace user role assignments in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/workplace/updateWorkplaceUserRole`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update Workplace User Role](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | body | `string` | no | Email address of the workplace user to update. |
| `phoneNumber` | body | `string` | no | Phone number of the workplace user to update. |
| `role` | body | `string` | yes | Target Clappia workplace role. |

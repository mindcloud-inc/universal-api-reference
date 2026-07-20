# Update Workplace User Details with Clappia

Updates workplace user details in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/workplace/updateWorkplaceUserDetails`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update Workplace User Details](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | body | `string` | no | Current email address of the workplace user to update. |
| `phoneNumber` | body | `string` | no | Current phone number of the workplace user to update. |
| `updatedDetails` | body | `object` | yes | Object containing the fields to update for the user. |

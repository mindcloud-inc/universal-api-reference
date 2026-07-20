# Update Workplace User Attributes with Clappia

Updates workplace user attributes in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/workplace/updateWorkplaceUserAttributes`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update Workplace User Attributes](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | body | `string` | no | Email address of the workplace user to update. |
| `phoneNumber` | body | `string` | no | Phone number of the workplace user to update. |
| `attributes` | body | `object` | yes | Object containing the workplace user attributes to apply. |

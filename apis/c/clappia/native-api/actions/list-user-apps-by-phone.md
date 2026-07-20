# List User Apps by Phone with Clappia

Retrieves user apps from Clappia by phone number.

## Endpoint

- **Method:** `GET`
- **Path:** `/workplace/getUserApps`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [List User Apps by Phone](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | query | `string` | yes | Phone number of the workplace user whose apps should be returned. |

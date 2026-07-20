# List User Apps by Email with Clappia

Retrieves user apps from Clappia by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/workplace/getUserApps`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [List User Apps by Email](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | query | `string` | yes | Email address of the workplace user whose apps should be returned. |

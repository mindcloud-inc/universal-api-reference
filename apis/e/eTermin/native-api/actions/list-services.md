# List Services with eTermin

Retrieves services from eTermin.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [List Services](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Service/get_api_service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageid` | query | `string` | no | Use the language code in which you want the name and description of the service (e.g., DE, EN, etc.) |
| `id` | query | `number` | no | ID of the service to get the information of a specific service |
| `ServiceGroupID` | query | `number` | no | Use if you want only services of a specific service group |
| `addimage` | query | `number` | no | true if you want to also get the image-data in your response |

# Get Contact Person with Alto

Retrieves a contact person from Alto by contact and person ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contactId/persons/:personId`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Contact Person](https://developers.vebraalto.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Unique Alto contact identifier. |
| `personId` | path | `string` | yes | Unique Alto person identifier within the contact. |

# Create Property with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `POST`
- **Path:** `/grny_properties`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Create Property](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/create-entity-web-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `grny_propertyid` | body | `string` | no | Optional deterministic GUID. Sent as grny_propertyid in the POST body; omit to let Dataverse assign an ID. Maximum length: 36. |
| `fields` | body | `object` | yes | Required writable Dataverse columns by logical name, including grny_aspireid. Do not repeat grny_propertyid inside Fields; use Record ID. |

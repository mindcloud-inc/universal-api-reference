# Create Contact with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Create Contact](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/create-entity-web-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactid` | body | `string` | no | Optional deterministic GUID. Sent as contactid in the POST body; omit to let Dataverse assign an ID. Maximum length: 36. |
| `fields` | body | `object` | yes | Required writable Dataverse columns by logical name, including grny_aspireid. Do not repeat contactid inside Fields; use Record ID. |

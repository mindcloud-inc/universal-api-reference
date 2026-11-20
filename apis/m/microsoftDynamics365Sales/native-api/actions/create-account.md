# Create Account with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Create Account](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/create-entity-web-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountid` | body | `string` | no | Optional deterministic GUID. Sent as accountid in the POST body; omit to let Dataverse assign an ID. Maximum length: 36. |
| `fields` | body | `object` | yes | Required writable Dataverse columns by logical name, including grny_aspireid. Do not repeat accountid inside Fields; use Record ID. |

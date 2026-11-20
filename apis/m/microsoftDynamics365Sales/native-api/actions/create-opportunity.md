# Create Opportunity with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `POST`
- **Path:** `/opportunities`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Create Opportunity](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/create-entity-web-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `grny_aspireid` | body | `number` | yes | Required positive int32 Aspire OpportunityID. Sent as Dynamics opportunity.grny_aspireid in the POST body; duplicate values are rejected by active alternate key grny_uniqueaspireid. |
| `fields` | body | `object` | yes | Required Opportunity JSON object using writable Dataverse logical column names. Include name (max 300). Use verified @odata.bind navigation properties for relationships. Omit grny_aspireid because it is in the URL; exclude statecode/statuscode and other unsupported fields. |

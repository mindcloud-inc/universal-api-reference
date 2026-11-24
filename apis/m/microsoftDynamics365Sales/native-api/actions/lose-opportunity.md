# Lose Opportunity with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `POST`
- **Path:** `/LoseOpportunity`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Lose Opportunity](https://learn.microsoft.com/en-us/dynamics365/developer/reference/mcp-tools/close_opportunity)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunityId` | body | `string` | no | Dynamics Opportunity GUID; provide this or Aspire Opportunity ID. |
| `aspireOpportunityId` | body | `number` | no | Aspire ID resolved by Dynamics alternate key grny_aspireid; provide this or Opportunity ID. |
| `status` | body | `number` | no | Win: 3. Lose: 4 (Canceled) or 5 (Out-Sold). |
| `subject` | body | `string` | no | Opportunity Close activity subject. |
| `actualEnd` | body | `string` | no | Calendar date exactly as YYYY-MM-DD; no timezone conversion. |
| `description` | body | `string` | no | Optional close description. |

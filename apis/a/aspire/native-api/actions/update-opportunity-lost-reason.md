# Update Opportunity Lost Reason with Aspire

Updates an existing opportunity lost reason in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `OpportunityLostReasons`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Opportunity Lost Reason](https://cloud-api.youraspire.com/swagger/index.html#/OpportunityLostReasons/OpportunityLostReasons_Update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `OpportunityLostReasonName` | body | `string` | no |
| `OpportunityLostReasonID` | body | `number` | yes |
| `Active` | body | `boolean` | no |

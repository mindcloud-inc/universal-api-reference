# Create Opportunity Lost Reason with Aspire

Creates a new opportunity lost reason in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `OpportunityLostReasons`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Opportunity Lost Reason](https://cloud-api.youraspire.com/swagger/index.html#/OpportunityLostReasons/OpportunityLostReasons_Create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `OpportunityLostReasonName` | body | `string` | yes |
| `Active` | body | `boolean` | yes |

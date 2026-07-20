# Create Estimate with Aspire

Retrieves takeoff groups from your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `Opportunities/EstimateImport`
- **Base URL:** `https://{environment}.youraspire.com/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `OpportunityId` | body | `list<number>` | yes |
| `TransitionToBidding` | body | `boolean` | no |
| `OpportunityServiceGroups` | body | `string` | no |

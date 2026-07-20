# Create Opportunity with Insightly

Creates a new opportunity in Insightly.

## Endpoint

- **Method:** `POST`
- **Path:** `{apiBaseUrl}Opportunities`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Create Opportunity](https://api.insightly.com/v3.1/Help#!/Opportunities/AddEntity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OPPORTUNITY_NAME` | body | `string` | yes | The opportunity name. |
| `OPPORTUNITY_STATE` | body | `string` | no | The opportunity state. |
| `BID_AMOUNT` | body | `number` | no | The bid amount for the opportunity. |
| `BID_CURRENCY` | body | `string` | no | The bid currency code. |
| `FORECAST_CLOSE_DATE` | body | `string` | no | The forecast close date in UTC. |
| `ORGANISATION_ID` | body | `number` | no | The related Organisation ID. |

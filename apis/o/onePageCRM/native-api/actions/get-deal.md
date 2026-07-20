# Get Deal with OnePageCRM

Retrieves a deal from OnePageCRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/deals/:deal_id`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [Get Deal](https://developer.onepagecrm.com/api/#/Deals/get_deals__deal_id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal_id` | path | `list<string>` | yes | ID of the deal to retrieve |
| `include_history` | query | `boolean` | no | Include deal stage history in the response |

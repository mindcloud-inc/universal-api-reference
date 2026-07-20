# List Channel Availability Rules with Channex

Retrieves channel availability rules from Channex.

## Endpoint

- **Method:** `GET`
- **Path:** `/channel_availability_rules`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [List Channel Availability Rules](https://docs.channex.io/api-v.1-documentation/availability-rules-collection#get-list-of-availabilty-rules)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[property_id]` | query | `string` | yes | Property UUID required by the channel availability rules list endpoint. |

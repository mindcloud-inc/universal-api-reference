# List Customers in a Segment with Customer.io

Retrieves customers in a segment from Customer.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/segments/:segment_id/membership`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [List Customers in a Segment](https://docs.customer.io/integrations/api/app/#tag/Segments/operation/getSegmentMembership)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `segment_id` | path | `number` | yes | The numeric ID of the segment whose members you want to list. |

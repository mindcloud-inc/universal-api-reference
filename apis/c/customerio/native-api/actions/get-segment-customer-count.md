# Get Segment Customer Count with Customer.io

Retrieves the customer count for a Customer.io segment.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/segments/:segment_id/customer_count`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Get Segment Customer Count](https://docs.customer.io/integrations/api/app/#tag/Segments/operation/getSegmentCount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `segment_id` | path | `list<number>` | yes | The identifier for the segment to inspect. |

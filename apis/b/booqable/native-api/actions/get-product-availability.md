# Get Product Availability with Booqable

Retrieves availability for a product in Booqable.

## Endpoint

- **Method:** `GET`
- **Path:** `/availabilities`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Get Product Availability](https://developers.booqable.com/#availabilities-fetch-availability-for-a-product)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[availabilities]` | query | `string` | no | Comma-separated availability fields to include instead of the default fields. |
| `meta[total][]` | query | `array<string>` | no | Aggregations to include in meta.total. |
| `filter[month]` | query | `number` | yes | Calendar month to inspect. |
| `filter[year]` | query | `number` | yes | Calendar year to inspect. |
| `filter[subject_id]` | query | `string` | yes | Product UUID to evaluate for booking availability. |
| `filter[day]` | query | `number` | no | Day of the month for time-based availability. |
| `filter[starts_at]` | query | `date` | no | Start timestamp for time-based availability. |
| `filter[duration_period]` | query | `string` | no | Time-slot duration period for day views. |
| `filter[interval]` | query | `number` | no | Minute interval for time-based availability. |
| `filter[use_business_hours]` | query | `boolean` | no | Limit time-based results to business hours. |
| `filter[location_id]` | query | `string` | no | Location UUID to scope the availability query. |

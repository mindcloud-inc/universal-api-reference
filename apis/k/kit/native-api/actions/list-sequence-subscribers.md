# List Sequence Subscribers with Kit

Lists subscribers for a Kit sequence.

## Endpoint

- **Method:** `GET`
- **Path:** `/sequences/:sequence_id/subscribers`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [List Sequence Subscribers](https://developers.kit.com/api-reference/sequences/list-subscribers-for-a-sequence)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sequence_id` | path | `number` | yes | Sequence ID from path parameter. |
| `status` | query | `string` | no | Filter by subscriber status. |
| `per_page` | query | `number` | no | Number of results per page (default 500, max 1000). |
| `after` | query | `string` | no | Fetch next page using end_cursor. |
| `before` | query | `string` | no | Fetch previous page using start_cursor. |
| `include_total_count` | query | `boolean` | no | Include total count in response. |
| `created_after` | query | `date` | no | Filter subscribers created after timestamp. |
| `created_before` | query | `date` | no | Filter subscribers created before timestamp. |
| `added_after` | query | `date` | no | Filter subscribers added to sequence after timestamp. |
| `added_before` | query | `date` | no | Filter subscribers added to sequence before timestamp. |

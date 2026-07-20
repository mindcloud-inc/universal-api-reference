# Bulk Lookup Universal People with RocketReach

Creates a RocketReach Universal bulk people lookup.

## Endpoint

- **Method:** `POST`
- **Path:** `/universal/person/bulk_lookup`
- **Base URL:** `https://api.rocketreach.co/api/v2`
- **Official documentation:** [Bulk Lookup Universal People](https://docs.rocketreach.co/reference/create_universal_person_bulk_lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queries` | body | `list<object>` | no | Up to 100 person lookup query objects to submit in one bulk request. |
| `profile_list` | body | `string` | no | Add specified contacts to this profile list. |
| `webhook_id` | body | `number` | no | Webhook ID to post lookup results when the bulk job completes. |

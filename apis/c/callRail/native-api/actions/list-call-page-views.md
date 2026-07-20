# List Call Page Views with CallRail

Retrieves page views for a CallRail call.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/a/:account_id/calls/:call_id/page_views.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [List Call Page Views](https://apidocs.callrail.com/#retrieving-all-page-views-for-a-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | The CallRail account ID. |
| `call_id` | path | `string` | yes | The CallRail call ID. |
| `time_zone` | query | `string` | no | Optional IANA time zone override for page view timestamps. |

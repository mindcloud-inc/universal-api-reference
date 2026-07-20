# List Sent Campaigns with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign/calendar`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [List Sent Campaigns](https://help.ortto.com/a-695-retrieve-a-list-of-sent-campaigns-calendar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | body | `object` | yes | Calendar window start with year and month keys. |
| `end` | body | `object` | yes | Calendar window end with year and month keys. |
| `timezone` | body | `string` | yes | IANA timezone used for the calendar window. |

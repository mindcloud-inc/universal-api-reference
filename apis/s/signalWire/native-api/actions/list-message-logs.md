# List Message Logs with SignalWire

Retrieves message logs from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/messaging/logs`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List Message Logs](https://signalwire.com/docs/apis/rest/message-logs/list-message-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_deleted` | query | `boolean` | no | Include logs for deleted activity. |
| `created_before` | query | `string` | no | Return logs for activity prior to this date. |
| `created_on` | query | `string` | no | Return logs for activity on this date. |
| `created_after` | query | `string` | no | Return logs for activity after this date. |

# List Voice Logs with SignalWire

Retrieves voice logs from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/voice/logs`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List Voice Logs](https://signalwire.com/docs/apis/rest/voice-logs/list-voice-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_deleted` | query | `boolean` | no | Include logs for deleted activity. |
| `created_before` | query | `string` | no | Return logs for activity prior to this date. |
| `created_on` | query | `string` | no | Return logs for activity on this date. |
| `created_after` | query | `string` | no | Return logs for activity after this date. |

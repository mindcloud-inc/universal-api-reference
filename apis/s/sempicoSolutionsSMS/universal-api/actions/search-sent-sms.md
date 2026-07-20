# Sempico Solutions SMS: Search Sent SMS



```
GET https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/search-sent-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sempico Solutions SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/search-sent-sms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/search-sent-sms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `MCC` | number | no | Optional mobile country code filter. |
| `MNC` | number | no | Optional mobile network code filter. |
| `sender` | string | no | Optional Sender ID filter. |
| `phone[]` | array<string> | no | Optional phone number filters. |
| `id_base[]` | array<number> | no | Optional group ID filters. |
| `time_period` | string | no | Optional SMS sending period filter, for example 2023-07-24 00:00:00 - 2023-07-24 23:59:59. |
| `type_sms` | list | no | Optional SMS type filter. Sempico documents sms, hlr, and mnp. One of: `0`, `1`, `2`. |
| `limit` | number | no | Optional number of sent SMS records to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id_state": 1,
      "num_parts": 1,
      "originator": "string",
      "part_no": 1,
      "phone": "string",
      "state": "string",
      "text_sms": "string",
      "time": "2026-05-07T12:00:00.000Z",
      "type_sms": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id_state` | number | Delivery/report state ID for a sent SMS record. |
| `num_parts` | number | Number of message parts. |
| `originator` | string | Sender/originator value. |
| `part_no` | number | Message part number. |
| `phone` | string | Recipient phone number. |
| `state` | string | Delivery state. |
| `text_sms` | string | SMS message text. |
| `time` | date | Record timestamp. |
| `type_sms` | string | SMS type. |

## Native endpoint

Through the native Sempico Solutions SMS API, this operation is `POST /sms-full-data` (base URL `https://restapi.sempico.solutions/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-sent-sms.md) for the provider-specific parameters and requirements.


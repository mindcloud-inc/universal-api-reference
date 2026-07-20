# Postman: Get Monitor

Retrieves details for a monitor from Postman.

```
GET https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-monitor?connectionId=$CONNECTION_ID&monitorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "monitorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-monitor?${params}`, {
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
| `monitorId` | string | yes | The monitor's ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "monitor": {
        "active": true,
        "collectionUid": "string",
        "environmentUid": "string",
        "id": "string",
        "name": "Ava Chen",
        "options": {
          "followRedirects": true,
          "strictSSL": true
        },
        "schedule": {
          "cron": "string",
          "nextRun": "2026-05-07T12:00:00.000Z",
          "timezone": "string"
        },
        "uid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `monitor.active` | boolean |  |
| `monitor.collectionUid` | string |  |
| `monitor.environmentUid` | string |  |
| `monitor.id` | string |  |
| `monitor.name` | string |  |
| `monitor.options.followRedirects` | boolean |  |
| `monitor.options.strictSSL` | boolean |  |
| `monitor.schedule.cron` | string |  |
| `monitor.schedule.nextRun` | date |  |
| `monitor.schedule.timezone` | string |  |
| `monitor.uid` | string |  |

## Native endpoint

Through the native Postman API, this operation is `GET /monitors/:monitorId` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monitor.md) for the provider-specific parameters and requirements.


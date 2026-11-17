# ECI Bolt: Get Job Event Token



```
GET https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/get-job-event-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/get-job-event-token?connectionId=$CONNECTION_ID&since=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "since": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/get-job-event-token?${params}`, {
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
| `since` | date | yes | Start date and time for the change history. Bolt receives an ISO 8601 timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventToken": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventToken` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ECI Bolt API, this operation is `GET /open/v1/jobs/events/at` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-event-token.md) for the provider-specific parameters and requirements.


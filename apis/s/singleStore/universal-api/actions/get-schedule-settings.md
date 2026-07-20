# SingleStore: Get Schedule Settings

Retrieves schedule settings from SingleStore.

```
GET https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/get-schedule-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SingleStore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/get-schedule-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/get-schedule-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "isScheduled": true,
      "offset": 1,
      "type": "string",
      "weekFlags": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number | Saved ingest schedule duration. |
| `isScheduled` | boolean | Whether scheduling is currently enabled. |
| `offset` | number | Saved ingest schedule offset. |
| `type` | string | Saved schedule type. |
| `weekFlags` | string | Weekday selection flags returned by the API. |

## Native endpoint

Through the native SingleStore API, this operation is `GET /config-sched` (base URL `https://{{credentials.flowEndpoint}}:30081/ingest/api/ingest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule-settings.md) for the provider-specific parameters and requirements.


# mfr Field Service Management: List Time Events

Retrieves time events from mfr Field Service Management.

```
GET https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-time-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-time-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-time-events?${params}`, {
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
      "contactId": 1,
      "description": "string",
      "endDateTime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "serviceRequestId": 1,
      "startDateTime": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "timeEventType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |
| `description` | string |  |
| `endDateTime` | date |  |
| `id` | number |  |
| `serviceRequestId` | number |  |
| `startDateTime` | date |  |
| `state` | string |  |
| `timeEventType` | string |  |

## Native endpoint

Through the native mfr Field Service Management API, this operation is `GET TimeEvents` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-events.md) for the provider-specific parameters and requirements.


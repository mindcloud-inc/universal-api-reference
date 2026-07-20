# SignalWire: List Conferences

Retrieves conferences from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-conferences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-conferences?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/list-conferences?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "current_participants": 1,
      "id": "string",
      "max_size": 1,
      "name": "Ava Chen",
      "project_id": "string",
      "region": "string",
      "status": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Creation timestamp. |
| `current_participants` | number | Current participants in the conference. |
| `id` | string | Unique identifier for the conference. |
| `max_size` | number | Maximum size of the conference. |
| `name` | string | Name of the conference. |
| `project_id` | string | Project ID of the conference. |
| `region` | string | Region of the conference. |
| `status` | string | Status of the conference. |
| `type` | string | Type of the conference. |
| `updated_at` | date | Updated timestamp. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /logs/conferences` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conferences.md) for the provider-specific parameters and requirements.


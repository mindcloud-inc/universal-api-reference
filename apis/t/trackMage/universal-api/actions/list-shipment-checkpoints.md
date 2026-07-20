# TrackMage: List Shipment Checkpoints

Retrieves shipment checkpoints for a shipment in TrackMage.

```
GET https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-shipment-checkpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-shipment-checkpoints?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-shipment-checkpoints?${params}`, {
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
| `id` | string | yes | Shipment identifier |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | The collection page number Default: `1`. |
| `itemsPerPage` | number | no | The number of items per page Default: `30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkpointDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "info": "string",
      "location": "string",
      "rel": "string",
      "shipment": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkpointDate` | date |  |
| `id` | string |  |
| `info` | string |  |
| `location` | string |  |
| `rel` | string |  |
| `shipment` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `GET /shipments/{id}/checkpoints` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipment-checkpoints.md) for the provider-specific parameters and requirements.


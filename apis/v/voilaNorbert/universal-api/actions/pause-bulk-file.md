# VoilaNorbert: Pause Bulk File

Pauses an active bulk file in VoilaNorbert.

```
PUT https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/pause-bulk-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoilaNorbert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/pause-bulk-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/pause-bulk-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The bulk file id to pause. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "created": 1,
      "enrich": true,
      "enrich_token": "string",
      "filename": "Ava Chen",
      "id": 1,
      "list_id": 1,
      "quantity": 1,
      "rerun_frequency": 1,
      "rerun_last_time": 1,
      "started": 1,
      "status": "string",
      "success": 1,
      "treated": 1,
      "updated": 1,
      "webhook": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `created` | number |  |
| `enrich` | boolean |  |
| `enrich_token` | string |  |
| `filename` | string |  |
| `id` | number |  |
| `list_id` | number |  |
| `quantity` | number |  |
| `rerun_frequency` | number |  |
| `rerun_last_time` | number |  |
| `started` | number |  |
| `status` | string |  |
| `success` | number |  |
| `treated` | number |  |
| `updated` | number |  |
| `webhook` | string |  |

## Native endpoint

Through the native VoilaNorbert API, this operation is `POST /massives/:id/pause` (base URL `https://api.voilanorbert.com/2018-01-08`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pause-bulk-file.md) for the provider-specific parameters and requirements.


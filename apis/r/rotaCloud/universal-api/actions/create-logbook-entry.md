# RotaCloud: Create Logbook Entry



```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-logbook-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-logbook-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-logbook-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": 1,
      "createdAt": "string",
      "createdBy": 1,
      "date": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "time": "string",
      "updatedAt": "string",
      "updatedBy": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number |  |
| `createdAt` | string |  |
| `createdBy` | number |  |
| `date` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `time` | string |  |
| `updatedAt` | string |  |
| `updatedBy` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v2/logbook` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-logbook-entry.md) for the provider-specific parameters and requirements.


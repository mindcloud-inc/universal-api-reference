# data.world: Create a Dataset

Creates a dataset in data.world.

```
POST https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/create-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a data.world `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/create-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/create-dataset', {
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
      "id": "string",
      "owner": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `owner` | string |  |
| `title` | string |  |

## Native endpoint

Through the native data.world API, this operation is `POST /datasets/{owner}` (base URL `https://api.data.world/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset.md) for the provider-specific parameters and requirements.


# Worksection: Create Project Group



```
POST https://connect.mindcloud.co/v1/universal/worksection/latest/actions/create-project-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksection `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/worksection/latest/actions/create-project-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worksection/latest/actions/create-project-group', {
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
      "name": "Ava Chen",
      "page": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `page` | string |  |

## Native endpoint

Through the native Worksection API, this operation is `POST /` (base URL `https://min7657.worksection.com/api/admin/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-group.md) for the provider-specific parameters and requirements.


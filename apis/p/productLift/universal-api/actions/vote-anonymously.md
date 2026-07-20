# ProductLift: Vote Anonymously



```
POST https://connect.mindcloud.co/v1/universal/productLift/latest/actions/vote-anonymously
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductLift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productLift/latest/actions/vote-anonymously" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productLift/latest/actions/vote-anonymously', {
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
      "createdAt": "string",
      "message": "string",
      "voter": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `message` | string |  |
| `voter` | string |  |

## Native endpoint

Through the native ProductLift API, this operation is `POST /posts/{key}/anonymous_votes/{anonymous_id}` (base URL `https://mindcloud.productlift.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/vote-anonymously.md) for the provider-specific parameters and requirements.


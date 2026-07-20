# Rasayel: Tag Channel User By Tag ID

Adds a tag to a Rasayel channel user by tag ID.

```
PUT https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/tag-channel-user-by-tag-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rasayel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/tag-channel-user-by-tag-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/tag-channel-user-by-tag-id', {
  method: 'PUT',
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
      "createdAt": 1,
      "id": 1,
      "tagColor": "string",
      "tagName": "Ava Chen",
      "updatedAt": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `id` | number |  |
| `tagColor` | string |  |
| `tagName` | string |  |
| `updatedAt` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Rasayel API, this operation is `POST /` (base URL `https://api.rasayel.io/api/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tag-channel-user-by-tag-id.md) for the provider-specific parameters and requirements.


# Kit: Add Tag to Subscriber

Adds a tag to a Kit subscriber.

```
PUT https://connect.mindcloud.co/v1/universal/kit/latest/actions/add-tag-to-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kit/latest/actions/add-tag-to-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tagId": 1,
  "subscriberId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kit/latest/actions/add-tag-to-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tagId": 1,
    "subscriberId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagId` | number | yes | Tag ID from the path parameter. |
| `subscriberId` | number | yes | Subscriber ID from the path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscriber": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriber` | object | Tagged subscriber payload. |

## Native endpoint

Through the native Kit API, this operation is `POST /tags/:tag_id/subscribers/:id` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tag-to-subscriber.md) for the provider-specific parameters and requirements.


# Inoreader: Update Feed

Updates an existing feed subscription in Inoreader.

```
PUT https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/update-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inoreader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/update-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "streamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/update-feed', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "streamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Subscription edit action such as unfollow, edit, or subscribe. |
| `streamId` | string | yes | Subscription stream ID to update. |
| `title` | string | no | Optional new subscription title. |
| `addFolder` | string | no | Optional folder label to add. |
| `removeFolder` | string | no | Optional folder label to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Provider acknowledgement returned by Inoreader for the subscription edit mutation. |

## Native endpoint

Through the native Inoreader API, this operation is `POST /subscription/edit` (base URL `https://www.inoreader.com/reader/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-feed.md) for the provider-specific parameters and requirements.


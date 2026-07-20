# Feedbin: Rename Tag

Renames an existing tag in Feedbin.

```
PUT https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/rename-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feedbin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/rename-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "oldName": "Ava Chen",
  "newName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/rename-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "oldName": "Ava Chen",
    "newName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `oldName` | string | yes | Existing tag name to rename. |
| `newName` | string | yes | New tag name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feed_id": 1,
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feed_id` | number |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Feedbin API, this operation is `POST tags.json` (base URL `https://api.feedbin.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-tag.md) for the provider-specific parameters and requirements.


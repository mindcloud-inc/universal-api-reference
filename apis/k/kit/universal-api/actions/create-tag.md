# Kit: Create Tag

Creates a new tag in Kit.

```
POST https://connect.mindcloud.co/v1/universal/kit/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kit/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kit/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the tag to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tag": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tag` | object | Created or existing tag object. |

## Native endpoint

Through the native Kit API, this operation is `POST /tags` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.


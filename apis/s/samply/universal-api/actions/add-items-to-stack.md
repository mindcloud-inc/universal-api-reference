# Samply: Add Items To Stack



```
PUT https://connect.mindcloud.co/v1/universal/samply/latest/actions/add-items-to-stack
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/samply/latest/actions/add-items-to-stack" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/samply/latest/actions/add-items-to-stack', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileid` | string | no | The Samply file, folder, or stack id. |
| `projectid` | string | no | The Samply project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": [
        {}
      ],
      "color": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "timeCreated": 1,
      "trashed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | array<object> |  |
| `color` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `timeCreated` | number |  |
| `trashed` | boolean |  |

## Native endpoint

Through the native Samply API, this operation is `POST /projects/:projectid/files/:fileid` (base URL `https://samply.app/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-items-to-stack.md) for the provider-specific parameters and requirements.


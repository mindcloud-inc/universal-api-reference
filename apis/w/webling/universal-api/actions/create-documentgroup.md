# Webling: Create Documentgroup



```
POST https://connect.mindcloud.co/v1/universal/webling/latest/actions/create-documentgroup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webling/latest/actions/create-documentgroup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Stage 3 Documents",
  "parentId": "114"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webling/latest/actions/create-documentgroup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Stage 3 Documents",
    "parentId": "114"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Title for the new document group. Example: `Stage 3 Documents`. |
| `parentId` | number | yes | Documentgroup ID that should own the new document group. Default: `114`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Webling API, this operation is `POST /documentgroup` (base URL `https://{{credentials.instanceDomain}}/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-documentgroup.md) for the provider-specific parameters and requirements.


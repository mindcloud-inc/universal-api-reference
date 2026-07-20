# Resource Guru: Update Resource

Updates an existing resource in Resource Guru.

```
PUT https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/update-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resource Guru `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/update-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "900584"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/update-resource', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "900584"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Resource ID. Default: `900584`. Example: `900584`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": 1,
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Resource color. |
| `id` | number | Resource ID. |
| `name` | string | Resource name. |
| `url` | string | Resource URL. |

## Native endpoint

Through the native Resource Guru API, this operation is `PUT /resources/:id` (base URL `https://api.resourceguruapp.com/v1/{{credentials.accountId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-resource.md) for the provider-specific parameters and requirements.


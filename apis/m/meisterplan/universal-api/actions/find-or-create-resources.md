# Meisterplan: Find Or Create Resources

Finds resources in Meisterplan, or creates them if needed.

```
POST https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/find-or-create-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/find-or-create-resources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/find-or-create-resources', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "resourceKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Resource ID |
| `resourceKey` | string | Resource key |

## Native endpoint

Through the native Meisterplan API, this operation is `POST /resources/findOrCreateResources` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-or-create-resources.md) for the provider-specific parameters and requirements.


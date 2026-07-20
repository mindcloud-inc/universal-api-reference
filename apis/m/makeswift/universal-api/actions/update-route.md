# Makeswift: Update Route



```
PUT https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeswift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "routeIdOrPathname": "Ava Chen",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-route', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "routeIdOrPathname": "Ava Chen",
    "siteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `routeIdOrPathname` | string | yes | Route ID or pathname to update. |
| `siteId` | string | yes | The site ID containing the route. |
| `pathname` | string | no | Updated pathname for the route. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skipValidation` | boolean | no | Skip route conflict validation when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "pathname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `object` | string |  |
| `pathname` | string |  |

## Native endpoint

Through the native Makeswift API, this operation is `PATCH /v2/routes/:routeIdOrPathname` (base URL `https://api.makeswift.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-route.md) for the provider-specific parameters and requirements.


# redirect.pizza: Update Redirect



```
PUT https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/update-redirect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/update-redirect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "sources[]": [
    "string"
  ],
  "destination": "string",
  "redirectType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/update-redirect', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "sources[]": ["string"],
    "destination": "string",
    "redirectType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the redirect to update. |
| `sources[]` | array<string> | yes | URLs to redirect from. |
| `destination` | string | yes | Destination URL for the redirect. |
| `redirectType` | string | yes | Redirect mode such as permanent or temporary. |
| `uriForwarding` | boolean | no | Whether to forward the request path. |
| `keepQueryString` | boolean | no | Whether to forward the query string. |
| `tracking` | boolean | no | Whether to collect analytics for the redirect. |
| `tags[]` | array<string> | no | Tags that categorize the redirect. |
| `notes` | string | no | Internal notes about the redirect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "destination": "string",
      "domains": [
        {}
      ],
      "id": 1,
      "keepQueryString": true,
      "notes": "string",
      "redirectType": "string",
      "sources": [
        {}
      ],
      "tags": [
        "string"
      ],
      "tracking": true,
      "updatedAt": "string",
      "uriForwarding": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `destination` | string |  |
| `domains` | array<object> |  |
| `id` | number |  |
| `keepQueryString` | boolean |  |
| `notes` | string |  |
| `redirectType` | string |  |
| `sources` | array<object> |  |
| `tags` | array<string> |  |
| `tracking` | boolean |  |
| `updatedAt` | string |  |
| `uriForwarding` | boolean |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `PUT /api/v1/redirects/{id}` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-redirect.md) for the provider-specific parameters and requirements.


# redirect.pizza: Create Redirect



```
POST https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/create-redirect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/create-redirect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sources[]": [
    "string"
  ],
  "destination": "string",
  "redirectType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/create-redirect', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `sources[]` | array<string> | yes | URLs to redirect from. |
| `destination` | string | yes | Destination URL for the redirect. |
| `redirectType` | string | yes | Redirect mode such as permanent or temporary. |
| `uriForwarding` | boolean | no | Whether to forward the request path. |
| `keepQueryString` | boolean | no | Whether to forward the query string. |
| `tracking` | boolean | no | Whether to collect analytics for the redirect. |
| `tags[]` | array<string> | no | Tags that categorize the redirect. |
| `notes` | string | no | Internal notes about the redirect. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `merge` | boolean | no | Merge into an existing redirect with the same destination when possible. |
| `upsert` | boolean | no | Update an existing redirect when a provided source already exists. |

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

Through the native redirect.pizza API, this operation is `POST /api/v1/redirects` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-redirect.md) for the provider-specific parameters and requirements.


# redirect.pizza: Get Redirect



```
GET https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-redirect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-redirect?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-redirect?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the redirect. |

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

Through the native redirect.pizza API, this operation is `GET /api/v1/redirects/{id}` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-redirect.md) for the provider-specific parameters and requirements.


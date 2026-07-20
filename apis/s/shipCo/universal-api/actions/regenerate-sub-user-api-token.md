# Ship&Co: Regenerate Sub User API Token



```
PUT https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/regenerate-sub-user-api-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship&Co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/regenerate-sub-user-api-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/regenerate-sub-user-api-token', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Ship&Co sub-user ID whose token should be regenerated. Ship&Co requires a 32-character sub-user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token` | string | Regenerated sub user API token. |

## Native endpoint

Through the native Ship&Co API, this operation is `POST /sub-users/:id` (base URL `https://api.shipandco.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/regenerate-sub-user-api-token.md) for the provider-specific parameters and requirements.


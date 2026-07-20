# Big Cartel: Create Category

Creates a category in Big Cartel.

```
POST https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/create-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Big Cartel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/create-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Big Cartel account ID. |
| `id` | string | no |  |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "name": "Ava Chen",
        "permalink": "https://example.com",
        "position": 1
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.name` | string |  |
| `attributes.permalink` | string |  |
| `attributes.position` | number |  |
| `id` | string |  |
| `links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Big Cartel API, this operation is `POST /v1/accounts/[:account-id]/categories` (base URL `https://api.bigcartel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-category.md) for the provider-specific parameters and requirements.


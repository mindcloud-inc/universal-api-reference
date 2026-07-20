# Klenty: Bulk Create Prospects

Creates prospects in bulk in Klenty.

```
POST https://connect.mindcloud.co/v1/universal/klenty/latest/actions/bulk-create-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/bulk-create-prospects" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prospects": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/klenty/latest/actions/bulk-create-prospects', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prospects": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prospects` | list<object> | yes | List of prospects to create. Each item supports the documented Create Prospect fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": [
        {
          "prospect": "string",
          "status": "string"
        }
      ],
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details[].prospect` | string |  |
| `details[].status` | string |  |
| `status` | boolean |  |

## Native endpoint

Through the native Klenty API, this operation is `POST /prospects` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-prospects.md) for the provider-specific parameters and requirements.


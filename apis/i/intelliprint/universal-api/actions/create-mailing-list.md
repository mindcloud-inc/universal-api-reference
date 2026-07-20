# Intelliprint: Create Mailing List



```
POST https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intelliprint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-mailing-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-mailing-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "address_validation": {},
      "created": 1,
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "recipients": 1,
      "variables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `address_validation` | object |  |
| `created` | number |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `recipients` | number |  |
| `variables` | array<object> |  |

## Native endpoint

Through the native Intelliprint API, this operation is `POST /mailing_lists` (base URL `https://api.intelliprint.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mailing-list.md) for the provider-specific parameters and requirements.


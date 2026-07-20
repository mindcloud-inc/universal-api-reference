# Lob: Verify US Address



```
POST https://connect.mindcloud.co/v1/universal/lob/latest/actions/verify-us-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lob/latest/actions/verify-us-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "primaryLine": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lob/latest/actions/verify-us-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "primaryLine": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `primaryLine` | string | yes | The primary delivery line to verify. |
| `city` | string | no | The city. Required when ZIP Code is not provided. |
| `state` | string | no | The ISO 3166-2 two-letter state code or subdivision name. Required when ZIP Code is not provided. |
| `zipCode` | string | no | The ZIP code. Can be used instead of City and State. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "components": {},
      "deliverability": "string",
      "deliverability_analysis": {},
      "id": "string",
      "last_line": "string",
      "object": "string",
      "primary_line": "string",
      "recipient": "string",
      "secondary_line": "string",
      "urbanization": "string",
      "valid_address": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `components` | object |  |
| `deliverability` | string |  |
| `deliverability_analysis` | object |  |
| `id` | string |  |
| `last_line` | string |  |
| `object` | string |  |
| `primary_line` | string |  |
| `recipient` | string |  |
| `secondary_line` | string |  |
| `urbanization` | string |  |
| `valid_address` | boolean |  |

## Native endpoint

Through the native Lob API, this operation is `POST /us_verifications` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-us-address.md) for the provider-specific parameters and requirements.


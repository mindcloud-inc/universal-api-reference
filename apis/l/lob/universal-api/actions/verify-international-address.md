# Lob: Verify International Address



```
POST https://connect.mindcloud.co/v1/universal/lob/latest/actions/verify-international-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lob/latest/actions/verify-international-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "primaryLine": "string",
  "country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lob/latest/actions/verify-international-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "primaryLine": "string",
    "country": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `primaryLine` | string | yes | The primary delivery line of the international address. |
| `country` | string | yes | The 2-letter ISO 3166 country code. |
| `recipient` | string | no | The intended recipient. |
| `secondaryLine` | string | no | The secondary delivery line. |
| `city` | string | no | The city name. |
| `state` | string | no | The state or province name. |
| `postalCode` | string | no | The postal code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "components": {},
      "country": "string",
      "coverage": "string",
      "deliverability": "string",
      "id": "string",
      "last_line": "string",
      "object": "string",
      "primary_line": "string",
      "recipient": "string",
      "secondary_line": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `components` | object |  |
| `country` | string |  |
| `coverage` | string |  |
| `deliverability` | string |  |
| `id` | string |  |
| `last_line` | string |  |
| `object` | string |  |
| `primary_line` | string |  |
| `recipient` | string |  |
| `secondary_line` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Lob API, this operation is `POST /intl_verifications` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-international-address.md) for the provider-specific parameters and requirements.


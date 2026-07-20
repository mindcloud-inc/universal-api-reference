# Lob: Bulk Verify International Addresses



```
POST https://connect.mindcloud.co/v1/universal/lob/latest/actions/bulk-verify-international-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lob/latest/actions/bulk-verify-international-addresses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addresses[]": [
    {}
  ],
  "addresses[].primaryLine": "string",
  "addresses[].country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lob/latest/actions/bulk-verify-international-addresses', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addresses[]": [{}],
    "addresses[].primaryLine": "string",
    "addresses[].country": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addresses[]` | array<object> | yes | An array of up to 20 international verification objects. |
| `addresses[].primaryLine` | string | yes | The primary delivery line for each international address. |
| `addresses[].country` | string | yes | The 2-letter ISO 3166 country code for each address. |
| `addresses[].recipient` | string | no | The recipient for each address. |
| `addresses[].secondaryLine` | string | no | The secondary delivery line for each address. |
| `addresses[].city` | string | no | The city for each address. |
| `addresses[].state` | string | no | The state or province for each address. |
| `addresses[].postalCode` | string | no | The postal code for each address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "errors": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `errors` | boolean |  |

## Native endpoint

Through the native Lob API, this operation is `POST /bulk/intl_verifications` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-verify-international-addresses.md) for the provider-specific parameters and requirements.


# Socket: Compare License Data with Policy

Compares package license data with a Socket policy.

```
PUT https://connect.mindcloud.co/v1/universal/socket/latest/actions/compare-license-data-with-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/socket/latest/actions/compare-license-data-with-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/compare-license-data-with-policy', {
  method: 'PUT',
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
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<object> |  |
| `items[].filepathOrProvenance` | array<string> |  |
| `items[].level` | string |  |
| `items[].purl` | string |  |
| `items[].spdxAtomOrExtraData` | string |  |
| `items[].violationExplanation` | string |  |

## Native endpoint

Through the native Socket API, this operation is `POST /license-policy` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-license-data-with-policy.md) for the provider-specific parameters and requirements.


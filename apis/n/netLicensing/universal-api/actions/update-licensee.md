# NetLicensing: Update Licensee

Updates an existing licensee in NetLicensing.

```
PUT https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/update-licensee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetLicensing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/update-licensee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/update-licensee', {
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
      "active": "string",
      "lists": {},
      "name": "Ava Chen",
      "number": "string",
      "productNumber": "string",
      "type": "string",
      "warningLevelSummary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `lists` | object |  |
| `name` | string |  |
| `number` | string |  |
| `productNumber` | string |  |
| `type` | string |  |
| `warningLevelSummary` | string |  |

## Native endpoint

Through the native NetLicensing API, this operation is `POST /licensee/{licenseeNumber}` (base URL `https://go.netlicensing.io/core/v2/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-licensee.md) for the provider-specific parameters and requirements.


# Federal Communications Commission: Update DBS Licensee Address

Updates an FCC DBS licensee address.

```
PUT https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/update-dbs-licensee-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Communications Commission `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/update-dbs-licensee-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/update-dbs-licensee-address', {
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
      "message": "string",
      "responseTime": 1,
      "results": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | FCC service response message. |
| `responseTime` | number | FCC service response time. |
| `results` | object | Endpoint-specific FCC result payload. |
| `status` | string | FCC service response status. |

## Native endpoint

Through the native Federal Communications Commission API, this operation is `POST /api/service/dbs/licenseeAddress/update` (base URL `https://publicfiles.fcc.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dbs-licensee-address.md) for the provider-specific parameters and requirements.


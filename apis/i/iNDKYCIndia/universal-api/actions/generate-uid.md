# IN-D KYC India: Generate UID

Creates a new KYC session UID in IN-D KYC India.

```
POST https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/generate-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IN-D KYC India `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/generate-uid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/generate-uid', {
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
      "desc": "string",
      "result": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `desc` | string | Description returned by IN-D. |
| `result` | object | UID generation result object. |
| `status` | string | Request status. |

## Native endpoint

Through the native IN-D KYC India API, this operation is `GET /api/upload/uid` (base URL `https://api.kyc.in-d.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-uid.md) for the provider-specific parameters and requirements.


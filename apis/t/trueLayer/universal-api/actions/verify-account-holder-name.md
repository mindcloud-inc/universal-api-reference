# TrueLayer: Verify Account Holder Name

Verifies an account holder name in TrueLayer.

```
POST https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/verify-account-holder-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/verify-account-holder-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/verify-account-holder-name', {
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
      "matched": true,
      "result": "string",
      "status": "string",
      "verification_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `matched` | boolean |  |
| `result` | string |  |
| `status` | string |  |
| `verification_id` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `POST /verification/v1/verify` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-account-holder-name.md) for the provider-specific parameters and requirements.


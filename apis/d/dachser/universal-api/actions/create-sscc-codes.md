# Dachser: Create SSCC Codes

Creates SSCC codes for shipments in Dachser.

```
POST https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-sscc-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-sscc-codes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-sscc-codes', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `count` | number | no | Number of SSCCs to generate. Maximum 100. Default: `1`. |
| `usePrefix` | boolean | no | Whether to return SSCCs with the 00 prefix. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ssccs": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ssccs` | array<string> |  |

## Native endpoint

Through the native Dachser API, this operation is `POST /rest/v2/ssccs` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sscc-codes.md) for the provider-specific parameters and requirements.


# Ship&Co: Upload Negotiated Rates



```
PUT https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/upload-negotiated-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship&Co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/upload-negotiated-rates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "rates[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/upload-negotiated-rates', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "rates[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Ship&Co carrier ID whose negotiated rates should be uploaded. Ship&Co requires a 17-character carrier ID. |
| `rates[]` | array<object> | yes | Negotiated rates table array to upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Upload result message returned by Ship&Co. |

## Native endpoint

Through the native Ship&Co API, this operation is `POST /carriers/:id/rates` (base URL `https://api.shipandco.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-negotiated-rates.md) for the provider-specific parameters and requirements.


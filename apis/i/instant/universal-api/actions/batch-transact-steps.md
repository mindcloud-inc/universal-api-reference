# Instant: Batch Transact Steps

Applies transaction steps to Instant records.

```
PUT https://connect.mindcloud.co/v1/universal/instant/latest/actions/batch-transact-steps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instant/latest/actions/batch-transact-steps" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "steps[]": [
    [
      "string"
    ]
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instant/latest/actions/batch-transact-steps', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "steps[]": [["string"]]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `steps[]` | array<array> | yes | Transaction step array to send to Instant. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tx-id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tx-id` | number | Transaction ID returned by Instant. |

## Native endpoint

Through the native Instant API, this operation is `POST /admin/transact` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-transact-steps.md) for the provider-specific parameters and requirements.


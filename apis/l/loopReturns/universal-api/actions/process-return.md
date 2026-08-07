# Loop Returns: Process Return

Process a return in Loop based on the return ID. Processing a return will archive it in Loop and fulfill any remaining outcomes, such as placing exchange orders or creating gift cards.

```
PUT https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/process-return
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loop Returns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/process-return" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "return_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/process-return', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "return_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `return_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors.message` | string |  |

## Native endpoint

Through the native Loop Returns API, this operation is `POST https://api.loopreturns.com/api/v1/warehouse/return/{{return_id}}/process` (base URL `https://api.loopreturns.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-return.md) for the provider-specific parameters and requirements.


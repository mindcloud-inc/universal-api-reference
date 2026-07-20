# Digit.ink: Add Batch To Stack



```
PUT https://connect.mindcloud.co/v1/universal/digitink/latest/actions/add-batch-to-stack
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digit.ink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/add-batch-to-stack" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stackUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitink/latest/actions/add-batch-to-stack', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stackUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stackUuid` | string | yes | Stack UUID path parameter. |
| `batchUuid` | string | no | Batch UUID to add to the stack. |
| `issued` | string | no | Issued timestamp to identify the batch to add. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchIds": [
        "string"
      ],
      "issuerUri": "string",
      "stackName": "Ava Chen",
      "stackUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchIds` | array<string> |  |
| `issuerUri` | string |  |
| `stackName` | string |  |
| `stackUuid` | string |  |

## Native endpoint

Through the native Digit.ink API, this operation is `POST /stacks/:stackUuid` (base URL `https://app.digit.ink/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-batch-to-stack.md) for the provider-specific parameters and requirements.


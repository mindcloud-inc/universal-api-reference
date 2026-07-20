# Kite Suite: Update a sequence by ID



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-a-sequence-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-a-sequence-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "body": {},
  "subject": "string",
  "nextMessage": "string",
  "attachments[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-a-sequence-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "body": {},
    "subject": "string",
    "nextMessage": "string",
    "attachments[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the sequence to update. |
| `body` | object | yes | Request body |
| `subject` | string | yes | The subject of the sequence. |
| `nextMessage` | string | yes | The next message in the sequence (if any). |
| `attachments[]` | array | yes | List of attachment URLs or IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Details of the updated sequence. |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/campaign/sequence/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-sequence-by-id.md) for the provider-specific parameters and requirements.


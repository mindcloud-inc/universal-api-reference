# Print Autopilot: Finish Documents

Updates document statuses in Print Autopilot.

```
PUT https://connect.mindcloud.co/v1/universal/printAutopilot/latest/actions/finish-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print Autopilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/printAutopilot/latest/actions/finish-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printAutopilot/latest/actions/finish-documents', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | no | Document status objects to finish. |
| `items[].id` | number | no |  |
| `items[].state` | string | no |  |
| `items[].errMsg` | string | no | Error message when the document state is failed. |

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
| `message` | string |  |

## Native endpoint

Through the native Print Autopilot API, this operation is `POST /finish-print-jobs` (base URL `https://printautopilot.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/finish-documents.md) for the provider-specific parameters and requirements.


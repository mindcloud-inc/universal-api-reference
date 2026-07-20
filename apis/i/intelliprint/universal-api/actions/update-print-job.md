# Intelliprint: Update Print Job



```
PUT https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/update-print-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intelliprint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/update-print-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/update-print-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Intelliprint print job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "confirmed": true,
      "created": 1,
      "id": "string",
      "object": "string",
      "reference": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `confirmed` | boolean |  |
| `created` | number |  |
| `id` | string |  |
| `object` | string |  |
| `reference` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Intelliprint API, this operation is `POST /prints/:id` (base URL `https://api.intelliprint.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-print-job.md) for the provider-specific parameters and requirements.


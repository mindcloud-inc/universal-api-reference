# SparkPost: Create Recipient List



```
POST https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/create-recipient-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/create-recipient-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "recipients[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/create-recipient-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "recipients[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique recipient list identifier. |
| `name` | string | no | Human-readable recipient list name. |
| `recipients[]` | array<object> | yes | Recipients included in the stored list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "totalAcceptedRecipients": 1,
      "totalRejectedRecipients": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `totalAcceptedRecipients` | number |  |
| `totalRejectedRecipients` | number |  |

## Native endpoint

Through the native SparkPost API, this operation is `POST /recipient-lists` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recipient-list.md) for the provider-specific parameters and requirements.


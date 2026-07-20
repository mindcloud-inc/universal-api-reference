# Trolley: Update Recipient

Updates an existing recipient in Trolley.

```
PUT https://connect.mindcloud.co/v1/universal/trolley/latest/actions/update-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trolley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/update-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trolley/latest/actions/update-recipient', {
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
| `id` | string | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "recipient": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `recipient` | object |  |

## Native endpoint

Through the native Trolley API, this operation is `PATCH /v1/recipients/:id` (base URL `https://api.trolley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-recipient.md) for the provider-specific parameters and requirements.


# Trolley: Create Recipient

Creates a new recipient in Trolley.

```
POST https://connect.mindcloud.co/v1/universal/trolley/latest/actions/create-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trolley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/create-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trolley/latest/actions/create-recipient', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes |  |
| `email` | string | yes |  |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |

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

Through the native Trolley API, this operation is `POST /v1/recipients` (base URL `https://api.trolley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recipient.md) for the provider-specific parameters and requirements.


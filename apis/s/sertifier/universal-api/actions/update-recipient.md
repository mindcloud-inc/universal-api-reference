# Sertifier: Update Recipient

Updates an existing recipient in Sertifier.

```
PUT https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipients[].id": "Recipient ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-recipient', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipients[].id": "Recipient ID"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipients[].id` | string | yes | Example: `Recipient ID`. |
| `recipients[].name` | string | no | Example: `Updated recipient name`. |
| `recipients[].email` | string | no | Example: `updated-recipient@example.com`. |
| `updateExistingCredentials` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "data": true,
      "hasError": true,
      "isUpgraded": true,
      "message": "string",
      "showPurchaseSheet": true,
      "upgradePlan": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object |  |
| `data` | boolean |  |
| `hasError` | boolean |  |
| `isUpgraded` | boolean |  |
| `message` | string |  |
| `showPurchaseSheet` | boolean |  |
| `upgradePlan` | object |  |

## Native endpoint

Through the native Sertifier API, this operation is `PUT /recipient` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-recipient.md) for the provider-specific parameters and requirements.


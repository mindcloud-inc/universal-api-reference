# Remindlo: Upsert Contact



```
POST https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/upsert-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remindlo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/upsert-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/upsert-contact', {
  method: 'POST',
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
| `campaignIds[]` | array<string> | no |  |
| `customFields` | object | no |  |
| `email` | string | no |  |
| `firstName` | string | no |  |
| `isRecurrent` | boolean | no |  |
| `lastName` | string | no |  |
| `lastServiceAt` | date | no |  |
| `marketingConsent` | boolean | no |  |
| `nextDueAt` | date | no |  |
| `note` | string | no |  |
| `phone` | string | no |  |
| `recurrentIntervalUnit` | string | no |  |
| `recurrentIntervalValue` | number | no |  |
| `tags[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "contact": {},
      "contact_id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `contact` | object |  |
| `contact_id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Remindlo API, this operation is `POST /contacts` (base URL `https://api.remindlo.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-contact.md) for the provider-specific parameters and requirements.


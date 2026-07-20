# Hunter: Add Sequence Recipient



```
POST https://connect.mindcloud.co/v1/universal/hunter/latest/actions/add-sequence-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/add-sequence-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hunter/latest/actions/add-sequence-recipient', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | Identifier of the sequence. |
| `emails` | list<string> | no | Email addresses to add to the sequence. |
| `leadIds` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recipientsAdded": 1,
      "skippedRecipients": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recipientsAdded` | number |  |
| `skippedRecipients` | array<object> |  |

## Native endpoint

Through the native Hunter API, this operation is `POST /campaigns/:campaignId/recipients` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-sequence-recipient.md) for the provider-specific parameters and requirements.


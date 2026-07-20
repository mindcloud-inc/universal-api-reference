# Reply: Push Contact To Sequence



```
PUT https://connect.mindcloud.co/v1/universal/reply/latest/actions/push-contact-to-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reply/latest/actions/push-contact-to-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": 1,
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reply/latest/actions/push-contact-to-sequence', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": 1,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | number | yes | Reply campaign identifier. |
| `email` | string | yes | Contact email to enroll in the sequence. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pushedProspectIds": [
        1
      ],
      "skippedByInvalidEmail": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pushedProspectIds` | array<number> | Prospect IDs that were added to the campaign. |
| `skippedByInvalidEmail` | number | Count of skipped prospects because their email was invalid. |

## Native endpoint

Through the native Reply API, this operation is `POST /v1/actions/pushtocampaign` (base URL `https://api.reply.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/push-contact-to-sequence.md) for the provider-specific parameters and requirements.


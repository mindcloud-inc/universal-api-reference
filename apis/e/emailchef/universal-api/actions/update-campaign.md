# Emailchef: Update Campaign

Updates an existing campaign in Emailchef.

```
PUT https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emailchef `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/update-campaign', {
  method: 'PUT',
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
| `campaignId` | string | yes | The Emailchef campaign ID. |
| `instanceIn.name` | string | no | Campaign name. |
| `instanceIn.subject` | string | no | Email subject. |
| `instanceIn.htmlBody` | string | no | HTML body. |
| `instanceIn.textBody` | string | no | Text body. |
| `instanceIn.senderId` | string | no | Sender ID. |
| `instanceIn.replyToId` | string | no | Reply-to sender ID. |
| `instanceIn.confirmationEmailAddress` | string | no | Confirmation email address. |
| `instanceIn.lists[]` | array<object> | no | Associated lists. |
| `instanceIn.lists[].listId` | string | no | List ID. |
| `instanceIn.lists[].segmentId` | string | no | Segment ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Emailchef API returns.

## Native endpoint

Through the native Emailchef API, this operation is `PUT campaigns/:id` (base URL `https://app.emailchef.com/apps/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.


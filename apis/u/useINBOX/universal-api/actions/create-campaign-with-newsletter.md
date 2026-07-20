# UseINBOX: Create Campaign With Newsletter

Creates a campaign from a newsletter in UseINBOX.

```
POST https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-campaign-with-newsletter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-campaign-with-newsletter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "newsletterId": "string",
  "senderAccountId": "string",
  "listType": 1,
  "lists[]": [
    "string"
  ],
  "plannedTime": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-campaign-with-newsletter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "newsletterId": "string",
    "senderAccountId": "string",
    "listType": 1,
    "lists[]": ["string"],
    "plannedTime": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `newsletterId` | string | yes | Newsletter ID to send as a campaign. |
| `senderAccountId` | string | yes | Sender account ID used for the campaign. |
| `listType` | number | yes | INBOX list type value for the campaign audience. |
| `lists[]` | array<string> | yes | Contact list IDs that should receive the campaign. Accepts multiple values as an array. |
| `plannedTime` | date | yes | Scheduled campaign send time. |
| `notifyWhenStart` | boolean | no | Whether INBOX should notify when the campaign starts. Default: `false`. |
| `notifyWhenEnd` | boolean | no | Whether INBOX should notify when the campaign ends. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "plannedTime": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "subject": "string",
      "updateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | date |  |
| `id` | string |  |
| `name` | string |  |
| `plannedTime` | date |  |
| `status` | number |  |
| `subject` | string |  |
| `updateTime` | date |  |

## Native endpoint

Through the native UseINBOX API, this operation is `POST /inbox/v1/campaigns` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign-with-newsletter.md) for the provider-specific parameters and requirements.


# Mailchimp: Update Campaign

Updates an existing campaign in Mailchimp.

```
PUT https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaign_id": "string",
  "settings": {},
  "settings.subject_line": "string",
  "settings.from_name": "Ava Chen",
  "settings.reply_to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaign_id": "string",
    "settings": {},
    "settings.subject_line": "string",
    "settings.from_name": "Ava Chen",
    "settings.reply_to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaign_id` | string | yes | The unique ID for the campaign. |
| `rss_opts` | object | no |  |
| `social_card` | object | no |  |
| `tracking` | object | no |  |
| `variate_settings` | object | no |  |
| `settings` | object | yes | Campaign settings object. |
| `recipients` | object | no | Campaign recipients object. |
| `settings.subject_line` | string | yes | Campaign email subject line. |
| `settings.from_name` | string | yes | From name used in campaign emails. |
| `settings.reply_to` | string | yes | Reply-to email address. |
| `recipients.list_id` | string | no | The unique audience (list) id for campaign recipients. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "2026-05-07T12:00:00.000Z",
      "emailsSent": 1,
      "id": "string",
      "recipients": {},
      "sendTime": "2026-05-07T12:00:00.000Z",
      "settings": {},
      "status": "string",
      "type": "string",
      "webId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | date |  |
| `emailsSent` | number |  |
| `id` | string |  |
| `recipients` | object |  |
| `sendTime` | date |  |
| `settings` | object |  |
| `status` | string |  |
| `type` | string |  |
| `webId` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `PATCH campaigns/:campaign_id` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.


# Mailchimp: Get Campaign

Retrieves a campaign from Mailchimp.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaign_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaign_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-campaign?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaign_id` | string | yes | The unique ID for the campaign. |
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `include_resend_shortcut_eligibility` | boolean | no |  |
| `include_resend_shortcut_usage` | boolean | no |  |

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

Through the native Mailchimp API, this operation is `GET campaigns/:campaign_id` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.


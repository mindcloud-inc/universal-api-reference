# Mailchimp: Get Campaign Report

Retrieves a campaign report from Mailchimp.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-campaign-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-campaign-report?connectionId=$CONNECTION_ID&campaign_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaign_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/get-campaign-report?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "abuseReports": 1,
      "bounces": {},
      "campaignTitle": "string",
      "clicks": {},
      "emailsSent": 1,
      "id": "string",
      "listId": "string",
      "listIsActive": true,
      "opens": {},
      "sendTime": "2026-05-07T12:00:00.000Z",
      "type": "string",
      "unsubscribed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abuseReports` | number |  |
| `bounces` | object |  |
| `campaignTitle` | string |  |
| `clicks` | object |  |
| `emailsSent` | number |  |
| `id` | string |  |
| `listId` | string |  |
| `listIsActive` | boolean |  |
| `opens` | object |  |
| `sendTime` | date |  |
| `type` | string |  |
| `unsubscribed` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET reports/:campaign_id` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-report.md) for the provider-specific parameters and requirements.


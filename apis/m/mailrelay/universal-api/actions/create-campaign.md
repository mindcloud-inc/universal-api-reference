# Mailrelay: Create Campaign

Creates a new campaign in Mailrelay.

```
POST https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "<html><body><p>Hello!</p></body></html>",
  "senderId": "1",
  "subject": "Spring Newsletter",
  "target": "groups"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "<html><body><p>Hello!</p></body></html>",
    "senderId": "1",
    "subject": "Spring Newsletter",
    "target": "groups"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupIds[]` | array<number> | no | Group IDs when target is `groups`. Example: `1,2`. |
| `html` | string | yes | Campaign HTML content. Example: `<html><body><p>Hello!</p></body></html>`. |
| `segmentId` | number | no | Segment ID when target is `segment`. Example: `12`. |
| `senderId` | number | yes | Sender ID for the campaign. Example: `1`. |
| `subject` | string | yes | Campaign subject. Example: `Spring Newsletter`. |
| `target` | list | yes | Who the campaign should be sent to. One of: `0`, `1`. Example: `groups`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analyticsUtmCampaign": "string",
      "campaignFolderId": 1,
      "editorType": "string",
      "groupIds": [
        1
      ],
      "html": "string",
      "id": 1,
      "previewText": "string",
      "replyTo": "string",
      "segmentId": 1,
      "senderId": 1,
      "subject": "string",
      "target": "string",
      "urlToken": true,
      "usePremailer": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analyticsUtmCampaign` | string |  |
| `campaignFolderId` | number |  |
| `editorType` | string |  |
| `groupIds` | array<number> |  |
| `html` | string |  |
| `id` | number |  |
| `previewText` | string |  |
| `replyTo` | string |  |
| `segmentId` | number |  |
| `senderId` | number |  |
| `subject` | string |  |
| `target` | string |  |
| `urlToken` | boolean |  |
| `usePremailer` | boolean |  |

## Native endpoint

Through the native Mailrelay API, this operation is `POST campaigns` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.


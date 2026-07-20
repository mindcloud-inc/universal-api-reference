# Mailrelay: Update Campaign

Updates an existing campaign in Mailrelay.

```
PUT https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupIds[]` | array<number> | no | Updated group IDs when target is `groups`. Example: `1,2`. |
| `html` | string | no | Updated campaign HTML content. |
| `id` | number | yes | The Mailrelay campaign ID. Example: `1`. |
| `segmentId` | number | no | Updated segment ID when target is `segment`. Example: `12`. |
| `senderId` | number | no | Updated sender ID for the campaign. Example: `1`. |
| `subject` | string | no | Updated campaign subject. |
| `target` | list | no | Updated campaign target. One of: `0`, `1`. Example: `groups`. |

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

Through the native Mailrelay API, this operation is `PATCH campaigns/:id` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.


# Mailrelay: List Campaigns

Retrieves campaigns from your Mailrelay account.

```
GET https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/list-campaigns?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Mailrelay API, this operation is `GET campaigns` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.


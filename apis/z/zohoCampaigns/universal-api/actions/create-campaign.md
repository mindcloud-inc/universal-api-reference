# Zoho Campaigns: Create Campaign

Creates a campaign in Zoho Campaigns.

```
POST https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignName": "MindCloud Stage 3 Campaign",
  "fromEmail": "gabrielrodrigues@mindcloud.co",
  "subject": "MindCloud Stage 3 Subject",
  "listDetails": "{3zd640b3cb30d7b8c0f065b2367cf90e3edd95bbab504ab6d5954d005b40879657:[]}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignName": "MindCloud Stage 3 Campaign",
    "fromEmail": "gabrielrodrigues@mindcloud.co",
    "subject": "MindCloud Stage 3 Subject",
    "listDetails": "{3zd640b3cb30d7b8c0f065b2367cf90e3edd95bbab504ab6d5954d005b40879657:[]}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignName` | string | yes | Name for the campaign. Example: `MindCloud Stage 3 Campaign`. |
| `fromEmail` | string | yes | Verified sender email address for the campaign. Example: `gabrielrodrigues@mindcloud.co`. |
| `subject` | string | yes | Subject line for the campaign. Example: `MindCloud Stage 3 Subject`. |
| `contentUrl` | string | no | Public HTML URL used as the campaign content source. Example: `https://www.example.com`. |
| `listDetails` | string | yes | List-to-segment mapping in Zoho's documented string format. Example: `{3zd640b3cb30d7b8c0f065b2367cf90e3edd95bbab504ab6d5954d005b40879657:[]}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topicId` | list<string> | no | Topic ID required on accounts that use Zoho's updated topic management. Example: `1234567890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignKey": "string",
      "code": "string",
      "message": "string",
      "status": "string",
      "uri": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignKey` | string | Created campaign key when the request succeeds. |
| `code` | string | Zoho result code. |
| `message` | string | Provider message for the campaign creation attempt. |
| `status` | string | Zoho status string for error payloads. |
| `uri` | string | Zoho endpoint URI. |
| `version` | string | Zoho API version. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `POST /createCampaign` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.


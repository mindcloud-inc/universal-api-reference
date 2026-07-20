# Zoho Campaigns: Create Topics

Creates marketing topics in Zoho Campaigns.

```
POST https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/create-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/create-topics" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "details": "{topic_name:Product Updates,topic_desc:Monthly news}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/create-topics', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "details": "{topic_name:Product Updates,topic_desc:Monthly news}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `details` | string | yes | Topic envelope in Zoho's documented `details` format. Example: `{topic_name:Product Updates,topic_desc:Monthly news}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "message": "string",
      "topicId": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Zoho result code. |
| `message` | string | Provider message for the topic creation attempt. |
| `topicId` | string | Created topic identifier. |
| `uri` | string | Zoho endpoint URI. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `POST /topics` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-topics.md) for the provider-specific parameters and requirements.


# BHuman: List Generated Videos by Campaign

Retrieves generated videos for a campaign in BHuman.

```
GET https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-generated-videos-by-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BHuman `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-generated-videos-by-campaign?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-generated-videos-by-campaign?${params}`, {
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
| `campaignId` | string | yes | The campaign ID to look up generated videos for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "result": {
        "total": 1,
        "videos": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `result.total` | number |  |
| `result.videos` | array |  |

## Native endpoint

Through the native BHuman API, this operation is `GET /ai_studio/generated_video_by_campaign_id` (base URL `https://studio.bhuman.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-generated-videos-by-campaign.md) for the provider-specific parameters and requirements.


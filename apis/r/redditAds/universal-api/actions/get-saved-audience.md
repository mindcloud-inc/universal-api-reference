# Reddit Lead Ads: Get Saved Audience

Retrieves a saved audience from Reddit Ads.

```
GET https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-saved-audience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-saved-audience?connectionId=$CONNECTION_ID&savedAudienceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "savedAudienceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-saved-audience?${params}`, {
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
| `savedAudienceId` | string | yes | Reddit Ads saved audience identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Saved audience identifier. |
| `name` | string | Saved audience name. |
| `status` | string | Saved audience status. |

## Native endpoint

Through the native Reddit Lead Ads API, this operation is `GET /saved_audiences/{saved_audience_id}` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-saved-audience.md) for the provider-specific parameters and requirements.


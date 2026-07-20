# Influencers.club: List Discovery Locations By Platform

Retrieves discovery locations for a platform from Influencers.club.

```
GET https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/list-discovery-locations-by-platform
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/list-discovery-locations-by-platform?connectionId=$CONNECTION_ID&platform=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "platform": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/list-discovery-locations-by-platform?${params}`, {
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
| `platform` | string | yes | Platform slug (for example: instagram, tiktok, youtube). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Supported location value for the selected platform. |

## Native endpoint

Through the native Influencers.club API, this operation is `GET /public/v1/discovery/classifier/locations/:platform/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-discovery-locations-by-platform.md) for the provider-specific parameters and requirements.


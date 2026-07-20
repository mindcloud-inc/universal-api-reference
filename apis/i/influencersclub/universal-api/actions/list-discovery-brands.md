# Influencers.club: List Discovery Brands

Retrieves discovery brand filters from Influencers.club.

```
GET https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/list-discovery-brands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/list-discovery-brands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/list-discovery-brands?${params}`, {
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
      "cleaned": "string",
      "full_name": "Ava Chen",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cleaned` | string | Normalized brand name. |
| `full_name` | string | Brand display name. |
| `username` | string | Brand account username. |

## Native endpoint

Through the native Influencers.club API, this operation is `GET /public/v1/discovery/classifier/brands/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-discovery-brands.md) for the provider-specific parameters and requirements.


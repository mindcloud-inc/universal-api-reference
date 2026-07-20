# Influencers.club: List Audience Brand Categories

Retrieves audience brand categories from Influencers.club.

```
GET https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/list-audience-brand-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/list-audience-brand-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/list-audience-brand-categories?${params}`, {
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
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Audience brand category name. |

## Native endpoint

Through the native Influencers.club API, this operation is `GET /public/v1/discovery/classifier/audience-brand-categories/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-audience-brand-categories.md) for the provider-specific parameters and requirements.


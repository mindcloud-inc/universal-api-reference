# Influencers.club: Enrich Creator By Email

Retrieves creator enrichment data from Influencers.club by email address.

```
GET https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/enrich-creator-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/enrich-creator-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/enrich-creator-by-email?${params}`, {
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
| `email` | string | yes | Creator email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_cost": 1,
      "result": {},
      "trial_searches_left": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_cost` | number | Credits consumed by this request. |
| `result` | object | Enriched creator profile resolved from email. |
| `trial_searches_left` | number | Remaining trial searches available. |

## Native endpoint

Through the native Influencers.club API, this operation is `POST /public/v1/creators/enrich/email/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-creator-by-email.md) for the provider-specific parameters and requirements.


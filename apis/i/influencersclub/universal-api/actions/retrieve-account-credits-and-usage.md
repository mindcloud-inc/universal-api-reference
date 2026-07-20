# Influencers.club: Retrieve Account Credits And Usage

Retrieves account credits and usage details from Influencers.club.

```
GET https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/retrieve-account-credits-and-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/retrieve-account-credits-and-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/retrieve-account-credits-and-usage?${params}`, {
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
      "credits_available": 1,
      "credits_used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_available` | number | Remaining credits available. |
| `credits_used` | number | Total credits consumed. |

## Native endpoint

Through the native Influencers.club API, this operation is `GET /public/v1/accounts/credits/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-account-credits-and-usage.md) for the provider-specific parameters and requirements.


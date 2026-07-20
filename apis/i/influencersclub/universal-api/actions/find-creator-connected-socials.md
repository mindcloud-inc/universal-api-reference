# Influencers.club: Find Creator Connected Socials

Finds verified connected social accounts for a creator in Influencers.club.

```
GET https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/find-creator-connected-socials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/find-creator-connected-socials?connectionId=$CONNECTION_ID&platform=string&handle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "platform": "string",
  "handle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/find-creator-connected-socials?${params}`, {
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
| `platform` | string | yes | Creator platform (for example instagram). |
| `handle` | string | yes | Creator handle without @. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_cost": 1,
      "result": [
        {}
      ],
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
| `result` | array<object> | Connected social profiles discovered for the creator. |
| `trial_searches_left` | number | Remaining trial searches available. |

## Native endpoint

Through the native Influencers.club API, this operation is `POST /public/v1/creators/socials/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-creator-connected-socials.md) for the provider-specific parameters and requirements.


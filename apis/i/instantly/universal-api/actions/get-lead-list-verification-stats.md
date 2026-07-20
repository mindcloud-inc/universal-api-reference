# Instantly: Get Lead List Verification Stats

Retrieves lead list verification stats from Instantly.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-lead-list-verification-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-lead-list-verification-stats?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-lead-list-verification-stats?${params}`, {
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
| `id` | string | yes | Lead list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "stats": {},
      "total_leads": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stats` | object |  |
| `total_leads` | number |  |

## Native endpoint

Through the native Instantly API, this operation is `GET /api/v2/lead-lists/:id/verification-stats` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-list-verification-stats.md) for the provider-specific parameters and requirements.


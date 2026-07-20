# Podscan: Get Sponsor Trend

Retrieves sponsor trend data from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-sponsor-trend
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-sponsor-trend?connectionId=$CONNECTION_ID&sponsor=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sponsor": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-sponsor-trend?${params}`, {
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
| `sponsor` | string | yes | The sponsor ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "period": "string",
      "sponsor_id": "string",
      "trend": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `period` | string |  |
| `sponsor_id` | string |  |
| `trend` | array<object> |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /sponsors/{sponsor}/trend` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sponsor-trend.md) for the provider-specific parameters and requirements.


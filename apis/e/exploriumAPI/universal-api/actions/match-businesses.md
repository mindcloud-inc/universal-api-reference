# Explorium: Match Businesses

Matches businesses in Explorium API.

```
GET https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/match-businesses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explorium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/match-businesses?connectionId=$CONNECTION_ID&businesses_to_match%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businesses_to_match[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/match-businesses?${params}`, {
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
| `businesses_to_match[]` | array<object> | yes | Businesses to match. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseContext": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseContext` | object | Explorium response metadata. |

## Native endpoint

Through the native Explorium API, this operation is `POST /v1/businesses/match` (base URL `https://api.explorium.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/match-businesses.md) for the provider-specific parameters and requirements.


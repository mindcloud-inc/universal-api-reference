# Waze Deep Links: Search Address

Generates a Waze deep link URL to search an address.

```
GET https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/search-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Waze Deep Links `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/search-address?connectionId=$CONNECTION_ID&q=66%20Acacia%20Avenue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "66 Acacia Avenue"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/search-address?${params}`, {
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
| `q` | string | yes | Address or place to search in Waze. Example: `66 Acacia Avenue`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | Generated Waze deep link URL. |

## Native endpoint

Through the native Waze Deep Links API, this operation is `GET https://waze.com/ul` (base URL `https://waze.com/ul`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-address.md) for the provider-specific parameters and requirements.


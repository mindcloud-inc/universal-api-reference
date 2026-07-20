# Waze Deep Links: Navigate To Favorite

Generates a Waze navigation URL to a saved favorite.

```
GET https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/navigate-to-favorite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Waze Deep Links `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/navigate-to-favorite?connectionId=$CONNECTION_ID&favorite=Home" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "favorite": "Home"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wazeDeepLinks/latest/actions/navigate-to-favorite?${params}`, {
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
| `favorite` | list | yes | Saved Waze favorite destination. One of: `Home`, `Work`. |

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

Through the native Waze Deep Links API, this operation is `GET https://waze.com/ul` (base URL `https://waze.com/ul`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/navigate-to-favorite.md) for the provider-specific parameters and requirements.


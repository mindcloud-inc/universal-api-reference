# Ron Swanson Quotes: Get Quotes

Retrieves multiple Ron Swanson quotes.

```
GET https://connect.mindcloud.co/v1/universal/ronSwansonQuotes/latest/actions/get-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ron Swanson Quotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ronSwansonQuotes/latest/actions/get-quotes?connectionId=$CONNECTION_ID&count=2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "count": "2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ronSwansonQuotes/latest/actions/get-quotes?${params}`, {
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
| `count` | number | yes | Number of random Ron Swanson quotes to return. Default: `2`. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "quote": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `quote` | string | Ron Swanson quote text. |

## Native endpoint

Through the native Ron Swanson Quotes API, this operation is `GET /quotes/:count` (base URL `https://ron-swanson-quotes.herokuapp.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quotes.md) for the provider-specific parameters and requirements.


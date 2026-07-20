# Sendible: Search Images



```
GET https://connect.mindcloud.co/v1/universal/sendible/latest/actions/search-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/search-images?connectionId=$CONNECTION_ID&integration=string&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "integration": "string",
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendible/latest/actions/search-images?${params}`, {
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
| `integration` | string | yes | Image provider slug such as Giphy or Pexels. |
| `search` | string | yes | Search term for the image provider. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
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
| `result` | array<object> |  |

## Native endpoint

Through the native Sendible API, this operation is `GET api/v3/images/search/{{integration}}.json` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-images.md) for the provider-specific parameters and requirements.


# Cloudinary: Search Resources

Finds resources in Cloudinary by search expression.

```
GET https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/search-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/search-resources?connectionId=$CONNECTION_ID&expression=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "expression": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/search-resources?${params}`, {
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
| `expression` | string | yes | The search expression to run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next_cursor": "string",
      "resources": [
        {}
      ],
      "time": 1,
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `next_cursor` | string |  |
| `resources` | array<object> |  |
| `time` | number |  |
| `total_count` | number |  |

## Native endpoint

Through the native Cloudinary API, this operation is `GET /resources/search` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-resources.md) for the provider-specific parameters and requirements.


# Browser Use: List Profiles

Retrieves profiles from Browser Use.

```
GET https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/list-profiles?${params}`, {
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
| `query` | string | no | Search profiles by name or user ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageNumber` | number | no | Page number, 1-indexed. Default: `1`. |
| `pageSize` | number | no | Number of profiles per page, maximum 100. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "pageNumber": 1,
      "pageSize": 1,
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `pageNumber` | number |  |
| `pageSize` | number |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Browser Use API, this operation is `GET /profiles` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-profiles.md) for the provider-specific parameters and requirements.


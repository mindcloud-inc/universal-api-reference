# Shuffler: Search Apps

Finds apps in Shuffler by search query.

```
GET https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/search-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/search-apps?connectionId=$CONNECTION_ID&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/search-apps?${params}`, {
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
| `search` | string | yes | App search string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reason": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reason` | array |  |
| `success` | boolean |  |

## Native endpoint

Through the native Shuffler API, this operation is `POST /apps/search` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-apps.md) for the provider-specific parameters and requirements.


# Element: Search User Directory

Finds users in Element by search term.

```
GET https://connect.mindcloud.co/v1/universal/element/latest/actions/search-user-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/element/latest/actions/search-user-directory?connectionId=$CONNECTION_ID&searchTerm=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchTerm": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/element/latest/actions/search-user-directory?${params}`, {
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
| `searchTerm` | string | yes | Case-insensitive term to match against the user directory. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limited": true,
      "results": [
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
| `limited` | boolean |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Element API, this operation is `POST /_matrix/client/v3/user_directory/search` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-user-directory.md) for the provider-specific parameters and requirements.


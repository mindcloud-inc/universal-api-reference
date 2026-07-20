# LastPass: Get Shared Folder Data

Retrieves shared folder data from LastPass.

```
GET https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-shared-folder-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LastPass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-shared-folder-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-shared-folder-data?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "give": true,
      "groups": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "readonly": true,
      "users": [
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
| `give` | boolean |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `readonly` | boolean |  |
| `users` | array<object> |  |

## Native endpoint

Through the native LastPass API, this operation is `POST /enterpriseapi.php` (base URL `https://lastpass.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shared-folder-data.md) for the provider-specific parameters and requirements.


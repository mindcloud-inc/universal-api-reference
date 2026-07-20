# Tricentis qTest: List User Groups

Retrieves user groups from Tricentis qTest.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-user-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-user-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-user-groups?${params}`, {
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
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
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
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Tricentis qTest API, this operation is `GET /groups` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-groups.md) for the provider-specific parameters and requirements.


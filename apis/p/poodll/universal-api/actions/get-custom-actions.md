# Poodll: Get Custom Actions

Retrieves available custom actions from Poodll.

```
GET https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-custom-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poodll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-custom-actions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-custom-actions?${params}`, {
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
      "action": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Poodll API, this operation is `POST {{credentials.baseUrl}}/webservice/rest/server.php` (base URL `{{credentials.baseUrl}}/webservice/rest/server.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-actions.md) for the provider-specific parameters and requirements.


# ITM Platform: Search Projects



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-projects?${params}`, {
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
      "accountId": 1,
      "code": "string",
      "description": "string",
      "id": 1,
      "internalCode": "string",
      "internalCostCenter": "string",
      "name": "Ava Chen",
      "no": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `code` | string |  |
| `description` | string |  |
| `id` | number |  |
| `internalCode` | string |  |
| `internalCostCenter` | string |  |
| `name` | string |  |
| `no` | string |  |

## Native endpoint

Through the native ITM Platform API, this operation is `POST /v2/projects/search` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-projects.md) for the provider-specific parameters and requirements.


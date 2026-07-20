# ITM Platform: Search Issues



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-issues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-issues?${params}`, {
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
      "changeInProjectCost": {},
      "changeInProjectScheduleDays": 1,
      "description": "string",
      "id": 1,
      "managementCost": {},
      "managementHours": "string",
      "manager": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changeInProjectCost` | object |  |
| `changeInProjectScheduleDays` | number |  |
| `description` | string |  |
| `id` | number |  |
| `managementCost` | object |  |
| `managementHours` | string |  |
| `manager` | object |  |
| `name` | string |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /v2/issues/search` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-issues.md) for the provider-specific parameters and requirements.


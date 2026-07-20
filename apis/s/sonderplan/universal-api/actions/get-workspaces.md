# Sonderplan: Get Workspaces



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-workspaces?${params}`, {
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
      "access": "string",
      "countryRegion": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "showPublicHoliday": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `countryRegion` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `showPublicHoliday` | boolean |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /workspace` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspaces.md) for the provider-specific parameters and requirements.


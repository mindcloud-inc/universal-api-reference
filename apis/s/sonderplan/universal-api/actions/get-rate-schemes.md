# Sonderplan: Get Rate Schemes



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-rate-schemes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-rate-schemes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-rate-schemes?${params}`, {
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
      "dayRate": 1,
      "description": "string",
      "hourRate": 1,
      "id": 1,
      "name": "Ava Chen",
      "typeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dayRate` | number |  |
| `description` | string |  |
| `hourRate` | number |  |
| `id` | number |  |
| `name` | string |  |
| `typeId` | number |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /rate-scheme` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rate-schemes.md) for the provider-specific parameters and requirements.


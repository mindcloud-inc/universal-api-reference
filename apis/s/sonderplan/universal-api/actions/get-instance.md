# Sonderplan: Get Instance



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-instance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-instance?${params}`, {
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
      "created": 1,
      "createdId": 1,
      "domain": "string",
      "name": "Ava Chen",
      "updated": 1,
      "updatedId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `createdId` | number |  |
| `domain` | string |  |
| `name` | string |  |
| `updated` | number |  |
| `updatedId` | number |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /instance` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-instance.md) for the provider-specific parameters and requirements.


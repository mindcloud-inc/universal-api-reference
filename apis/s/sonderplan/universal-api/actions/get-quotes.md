# Sonderplan: Get Quotes



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-quotes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-quotes?${params}`, {
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
      "client": {},
      "date": 1,
      "dateTimeIso": "string",
      "expiryDate": 1,
      "id": 1,
      "number": "string",
      "prefix": "string",
      "project": {},
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `date` | number |  |
| `dateTimeIso` | string |  |
| `expiryDate` | number |  |
| `id` | number |  |
| `number` | string |  |
| `prefix` | string |  |
| `project` | object |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /quote` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quotes.md) for the provider-specific parameters and requirements.


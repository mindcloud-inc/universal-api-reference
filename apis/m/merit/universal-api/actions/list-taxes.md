# Merit: List Taxes



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-taxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-taxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-taxes?${params}`, {
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
      "code": "string",
      "countryCode": {},
      "countryId": 1,
      "id": "string",
      "name": "Ava Chen",
      "nameEN": "Ava Chen",
      "nameRU": "Ava Chen",
      "nonActive": true,
      "taxPct": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `countryCode` | object |  |
| `countryId` | number |  |
| `id` | string |  |
| `name` | string |  |
| `nameEN` | string |  |
| `nameRU` | string |  |
| `nonActive` | boolean |  |
| `taxPct` | number |  |

## Native endpoint

Through the native Merit API, this operation is `POST v1/gettaxes` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-taxes.md) for the provider-specific parameters and requirements.


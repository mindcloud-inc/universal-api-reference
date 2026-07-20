# Sonderplan: Get Invoice Templates



```
GET https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-invoice-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sonderplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-invoice-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonderplan/latest/actions/get-invoice-templates?${params}`, {
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
      "default": true,
      "id": 1,
      "logo": {},
      "name": "Ava Chen",
      "title": "string",
      "typeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default` | boolean |  |
| `id` | number |  |
| `logo` | object |  |
| `name` | string |  |
| `title` | string |  |
| `typeId` | number |  |

## Native endpoint

Through the native Sonderplan API, this operation is `GET /invoice-template` (base URL `https://api.sonderplan.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-templates.md) for the provider-specific parameters and requirements.


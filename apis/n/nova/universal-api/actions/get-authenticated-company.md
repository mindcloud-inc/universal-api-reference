# Nova: Get Authenticated Company



```
GET https://connect.mindcloud.co/v1/universal/nova/latest/actions/get-authenticated-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nova/latest/actions/get-authenticated-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nova/latest/actions/get-authenticated-company?${params}`, {
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
      "company_id": 1,
      "company_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | number | Authenticated Nova company identifier. |
| `company_name` | string | Authenticated Nova company name. |

## Native endpoint

Through the native Nova API, this operation is `GET /admin/api/auth` (base URL `https://app.n0va.com/v1/la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-company.md) for the provider-specific parameters and requirements.


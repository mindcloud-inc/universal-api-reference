# B2B Wave: List VAT Groups

Retrieves VAT groups from B2B Wave.

```
GET https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-vat-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a B2B Wave `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-vat-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-vat-groups?${params}`, {
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
      "id": 1,
      "is_default": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `is_default` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native B2B Wave API, this operation is `GET /vat_groups` (base URL `{{credentials.storeUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vat-groups.md) for the provider-specific parameters and requirements.


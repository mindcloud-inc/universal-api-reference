# Scoro: List Finance Objects

Retrieves finance objects from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-finance-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-finance-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-finance-objects?${params}`, {
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
      "name": "Ava Chen",
      "object_id": 1,
      "object_symbol": "string",
      "parent_group_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `object_id` | number |  |
| `object_symbol` | string |  |
| `parent_group_name` | string |  |

## Native endpoint

Through the native Scoro API, this operation is `POST financeObjects/list` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-finance-objects.md) for the provider-specific parameters and requirements.


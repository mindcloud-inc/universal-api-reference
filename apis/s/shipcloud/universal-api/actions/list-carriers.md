# Shipcloud: List Carriers

Retrieves carriers from Shipcloud.

```
GET https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-carriers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-carriers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-carriers?${params}`, {
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
      "additional_services": [
        "string"
      ],
      "display_name": "Ava Chen",
      "name": "Ava Chen",
      "package_types": [
        "string"
      ],
      "services": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additional_services` | array<string> |  |
| `display_name` | string |  |
| `name` | string |  |
| `package_types` | array<string> |  |
| `services` | array<string> |  |

## Native endpoint

Through the native Shipcloud API, this operation is `GET /carriers` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-carriers.md) for the provider-specific parameters and requirements.


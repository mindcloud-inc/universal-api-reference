# Revel Digital: List Device Groups



```
GET https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-device-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-device-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-device-groups?${params}`, {
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
      "children": [
        {}
      ],
      "count": 1,
      "family": 1,
      "id": "string",
      "level": 1,
      "name": "Ava Chen",
      "organization_count": 1,
      "parent_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | array<object> |  |
| `count` | number |  |
| `family` | number |  |
| `id` | string |  |
| `level` | number |  |
| `name` | string |  |
| `organization_count` | number |  |
| `parent_id` | string |  |

## Native endpoint

Through the native Revel Digital API, this operation is `GET /devices/groups` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-device-groups.md) for the provider-specific parameters and requirements.


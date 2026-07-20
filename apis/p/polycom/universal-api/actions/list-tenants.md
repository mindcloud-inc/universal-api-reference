# Polycom: List Tenants

Lists Poly Lens tenants with member, device, and room totals.

```
GET https://connect.mindcloud.co/v1/universal/polycom/latest/actions/list-tenants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polycom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polycom/latest/actions/list-tenants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polycom/latest/actions/list-tenants?${params}`, {
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
      "deviceCount": 1,
      "id": "string",
      "memberCount": 1,
      "name": "Ava Chen",
      "roomData": {
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deviceCount` | number |  |
| `id` | string |  |
| `memberCount` | number |  |
| `name` | string |  |
| `roomData.total` | number |  |

## Native endpoint

Through the native Polycom API, this operation is `POST /graphql` (base URL `https://api.silica-prod01.io.lens.poly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tenants.md) for the provider-specific parameters and requirements.


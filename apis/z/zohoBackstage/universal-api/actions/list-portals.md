# Zoho Backstage: List Portals



```
GET https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-portals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-portals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-portals?${params}`, {
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
      "domain": "string",
      "id": "string",
      "isDefault": true,
      "name": "Ava Chen",
      "ownerEmail": "ava@example.com",
      "ownerName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `ownerEmail` | string |  |
| `ownerName` | string |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `GET /v3/portals` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-portals.md) for the provider-specific parameters and requirements.


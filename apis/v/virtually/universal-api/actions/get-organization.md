# Virtually: Get Organization

Retrieves organization details from your Virtually workspace.

```
GET https://connect.mindcloud.co/v1/universal/virtually/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/virtually/latest/actions/get-organization?${params}`, {
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
      "color": {},
      "createdAt": 1,
      "description": "string",
      "imageUri": {},
      "isSRM": true,
      "name": "Ava Chen",
      "orgId": "string",
      "ownerEmail": "ava@example.com",
      "ownerPhone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | object |  |
| `createdAt` | number |  |
| `description` | string |  |
| `imageUri` | object |  |
| `isSRM` | boolean |  |
| `name` | string |  |
| `orgId` | string |  |
| `ownerEmail` | string |  |
| `ownerPhone` | object |  |

## Native endpoint

Through the native Virtually API, this operation is `GET /api/v2/orgs/:orgId` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.


# Prembly: Get Custom Package Detail

Retrieves a custom package from Prembly.

```
GET https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-custom-package-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-custom-package-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-custom-package-detail?${params}`, {
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
      "allow_candidate_payment": true,
      "check_types": [
        "string"
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "is_active": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_candidate_payment` | boolean |  |
| `check_types[]` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `is_active` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `GET /api/v1/api/bgc/packages/:packageId` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-package-detail.md) for the provider-specific parameters and requirements.


# HR Partner: List Performance Reviews



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-performance-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-performance-reviews?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-performance-reviews?${params}`, {
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
      "assignedAt": "2026-05-07T12:00:00.000Z",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "employee": {},
      "id": 1,
      "responses": [
        {}
      ],
      "reviewDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "template": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedAt` | date |  |
| `completedAt` | date |  |
| `employee` | object |  |
| `id` | number |  |
| `responses` | array<object> |  |
| `reviewDate` | date |  |
| `status` | string |  |
| `template` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /performances` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-performance-reviews.md) for the provider-specific parameters and requirements.


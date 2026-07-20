# BulkSMS: Get Profile

Retrieves your account profile from BulkSMS.

```
GET https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BulkSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulkSMS/latest/actions/get-profile?${params}`, {
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
      "commerce": {},
      "company": {},
      "created": "2026-05-07T12:00:00.000Z",
      "credits": {},
      "id": "string",
      "originAddresses": {},
      "quota": {},
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commerce` | object |  |
| `company` | object |  |
| `created` | date |  |
| `credits` | object |  |
| `id` | string |  |
| `originAddresses` | object |  |
| `quota` | object |  |
| `username` | string |  |

## Native endpoint

Through the native BulkSMS API, this operation is `GET /profile` (base URL `https://api.bulksms.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.


# Trackabi: Get Company Details

Retrieves company details from Trackabi.

```
GET https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-company-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-company-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-company-details?${params}`, {
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
      "address": "string",
      "alias": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Company address. |
| `alias` | string | Company alias. |
| `email` | string | Company email address. |
| `name` | string | Company name. |
| `phone` | string | Company phone number. |

## Native endpoint

Through the native Trackabi API, this operation is `GET /api/v1/company/profile` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-details.md) for the provider-specific parameters and requirements.


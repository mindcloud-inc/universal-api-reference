# Eventee: List Partners

Retrieves partners from Eventee.

```
GET https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-partners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-partners?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-partners?${params}`, {
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
      "company": "string",
      "description": "string",
      "email": "ava@example.com",
      "exhibitorInfo": {},
      "id": 1,
      "phone": "string",
      "sponsorInfo": {},
      "web": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Partner address. |
| `company` | string | Partner company name. |
| `description` | string | Partner description. |
| `email` | string | Partner email. |
| `exhibitorInfo` | object | Exhibitor-specific info. |
| `id` | number | Partner ID. |
| `phone` | string | Partner phone number. |
| `sponsorInfo` | object | Sponsor-specific info. |
| `web` | string | Partner website URL. |

## Native endpoint

Through the native Eventee API, this operation is `GET /partners` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-partners.md) for the provider-specific parameters and requirements.


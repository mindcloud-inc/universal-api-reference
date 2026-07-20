# Launch27: Get Booking Form

Retrieves a booking form from Launch27.

```
GET https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-booking-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-booking-form?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-booking-form?${params}`, {
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
      "content_areas": {},
      "headings": [
        {}
      ],
      "paragraphs": {},
      "settings": {},
      "system_fields": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_areas` | object |  |
| `headings` | array<object> |  |
| `paragraphs` | object |  |
| `settings` | object |  |
| `system_fields` | object |  |

## Native endpoint

Through the native Launch27 API, this operation is `GET booking/form` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking-form.md) for the provider-specific parameters and requirements.


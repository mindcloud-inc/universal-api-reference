# Navigatr: List User Communities



```
GET https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-user-communities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Navigatr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-user-communities?connectionId=$CONNECTION_ID&userId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-user-communities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | Use 0 for the current user, or a specific user ID such as 19524 when needed. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "banner_url": "https://example.com",
          "city": "string",
          "country": "string",
          "email": "ava@example.com",
          "enable_members": true,
          "external_url": "https://example.com",
          "featured": true,
          "id": 1,
          "image_url": "https://example.com",
          "is_default": true,
          "is_demo": true,
          "is_verified": true,
          "name": "Ava Chen",
          "organisation_name": "Ava Chen",
          "phone": "string",
          "short_name": "Ava Chen",
          "status": "string",
          "time_created": "2026-05-07T12:00:00.000Z",
          "time_updated": "2026-05-07T12:00:00.000Z",
          "time_verified": "2026-05-07T12:00:00.000Z",
          "type": "string",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].banner_url` | string | Community banner URL |
| `[].city` | string | Community city |
| `[].country` | string | Community country |
| `[].email` | string | Community email |
| `[].enable_members` | boolean | Whether community members are enabled |
| `[].external_url` | string | External website URL |
| `[].featured` | boolean | Whether this community is featured |
| `[].id` | number | Community ID |
| `[].image_url` | string | Community image URL |
| `[].is_default` | boolean | Whether this is the default community |
| `[].is_demo` | boolean | Whether this is a demo community |
| `[].is_verified` | boolean | Whether this community is verified |
| `[].name` | string | Community name |
| `[].organisation_name` | string | Organisation name |
| `[].phone` | string | Community phone number |
| `[].short_name` | string | Community short name |
| `[].status` | string | Community status |
| `[].time_created` | date | Creation timestamp |
| `[].time_updated` | date | Last update timestamp |
| `[].time_verified` | date | Verification timestamp |
| `[].type` | string | Community type |
| `[].url` | string | Public community URL |

## Native endpoint

Through the native Navigatr API, this operation is `GET /user_detail/:user_id/communities` (base URL `https://api.navigatr.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-communities.md) for the provider-specific parameters and requirements.


# Lnk.Bio: Retrieve Basic Profile Info

Retrieves the authenticated user's profile from Lnk.Bio.

```
GET https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/retrieve-basic-profile-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lnk.Bio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/retrieve-basic-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lnkBio/latest/actions/retrieve-basic-profile-info?${params}`, {
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
      "errors": [
        "string"
      ],
      "info": {
        "profile_pic": "string",
        "url": "https://example.com",
        "username": "Ava Chen"
      },
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> | Errors returned by the Lnk.Bio API. |
| `info.profile_pic` | string | The public profile picture URL. |
| `info.url` | string | The public URL of the authenticated profile. |
| `info.username` | string | The Lnk.Bio username, including the @ prefix. |
| `status` | boolean | Whether the profile request succeeded. |

## Native endpoint

Through the native Lnk.Bio API, this operation is `GET /me` (base URL `https://lnk.bio/oauth/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-basic-profile-info.md) for the provider-specific parameters and requirements.


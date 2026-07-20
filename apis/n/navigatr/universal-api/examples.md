# Navigatr Universal API Examples

These examples use the MindCloud API key and Navigatr connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Detail

Retrieves user details from Navigatr.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/get-user-detail?connectionId=$CONNECTION_ID&userId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/get-user-detail?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "avatar_url": "https://example.com",
      "bio": "string",
      "communities": [
        {
          "id": 1,
          "name": "Ava Chen",
          "url": "https://example.com"
        }
      ],
      "emails": [
        {
          "email": "ava@example.com",
          "is_primary": true,
          "is_verified": true,
          "user_id": 1
        }
      ],
      "firstname": "Ava",
      "id": 1,
      "interests": [
        "string"
      ],
      "lastname": "Chen",
      "learning_styles": [
        "string"
      ],
      "providers": [
        {
          "id": 1,
          "name": "Ava Chen",
          "url": "https://example.com"
        }
      ],
      "role": "string",
      "status": "string",
      "time_created": "2026-05-07T12:00:00.000Z",
      "time_updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get User Detail action reference](actions/get-user-detail.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/navigatr/latest/actions/get-user-detail).

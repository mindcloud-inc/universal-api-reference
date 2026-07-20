# Yandex ID Universal API Examples

These examples use the MindCloud API key and Yandex ID connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yandexID/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yandexID/latest/actions/get-authenticated-user?${params}`, {
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
      "birthday": "string",
      "clientId": "string",
      "defaultAvatarId": "string",
      "defaultEmail": "ava@example.com",
      "displayName": "Ava Chen",
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "id": "string",
      "isAvatarEmpty": true,
      "lastName": "Chen",
      "login": "string",
      "psuid": "string",
      "realName": "Ava Chen",
      "sex": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yandexID/latest/actions/get-authenticated-user).

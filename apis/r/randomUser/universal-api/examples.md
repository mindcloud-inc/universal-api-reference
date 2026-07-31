# Random User Universal API Examples

These examples use the MindCloud API key and Random User connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Random Users



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomUser/latest/actions/generate-random-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/randomUser/latest/actions/generate-random-users?${params}`, {
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
      "info": {
        "page": 1,
        "results": 1,
        "seed": "string",
        "version": "string"
      },
      "results": [
        {
          "cell": "string",
          "dob": {
            "age": 1,
            "date": "2026-05-07T12:00:00.000Z"
          },
          "email": "ava@example.com",
          "gender": "string",
          "id": {
            "name": "Ava Chen",
            "value": "string"
          },
          "location": {
            "city": "string",
            "coordinates": {
              "latitude": "string",
              "longitude": "string"
            },
            "country": "string",
            "state": "string",
            "street": {
              "name": "Ava Chen",
              "number": 1
            },
            "timezone": {
              "description": "string",
              "offset": "string"
            }
          },
          "login": {
            "password": "string",
            "username": "Ava Chen",
            "uuid": "string"
          },
          "name": {
            "first": "Ava Chen",
            "last": "Ava Chen",
            "title": "Ava Chen"
          },
          "nat": "string",
          "phone": "string",
          "picture": {
            "large": "string",
            "medium": "string",
            "thumbnail": "string"
          },
          "registered": {
            "age": 1,
            "date": "2026-05-07T12:00:00.000Z"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Generate Random Users action reference](actions/generate-random-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/randomUser/latest/actions/generate-random-users).

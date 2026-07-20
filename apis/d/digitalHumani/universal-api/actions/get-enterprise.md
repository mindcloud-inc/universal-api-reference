# Digital Humani: Get Enterprise

Retrieves an enterprise from Digital Humani by ID.

```
GET https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-enterprise
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Humani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-enterprise?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-enterprise?${params}`, {
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
      "contact": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "rel": {
        "users": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.email` | string |  |
| `contact.name` | string |  |
| `created` | date |  |
| `id` | string |  |
| `name` | string |  |
| `rel.users` | string |  |

## Native endpoint

Through the native Digital Humani API, this operation is `GET /enterprise/:id` (base URL `https://api.digitalhumani.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enterprise.md) for the provider-specific parameters and requirements.


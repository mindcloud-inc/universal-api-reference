# CallPage: Get User

Retrieves a single user from CallPage.

```
GET https://connect.mindcloud.co/v1/universal/callPage/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callPage/latest/actions/get-user?${params}`, {
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
| `id` | number | no |  |
| `email` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activatedAt": "string",
      "avatar": {},
      "callerId": {
        "activatedAt": {},
        "id": 1,
        "updatedAt": "string"
      },
      "email": "ava@example.com",
      "id": 1,
      "lastOnline": {},
      "name": "Ava Chen",
      "parentId": 1,
      "role": {
        "slug": "string"
      },
      "tel": "string",
      "telExtension": {},
      "telFormatted": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activatedAt` | string |  |
| `avatar` | object |  |
| `callerId.activatedAt` | object |  |
| `callerId.id` | number |  |
| `callerId.updatedAt` | string |  |
| `email` | string |  |
| `id` | number |  |
| `lastOnline` | object |  |
| `name` | string |  |
| `parentId` | number |  |
| `role.slug` | string |  |
| `tel` | string |  |
| `telExtension` | object |  |
| `telFormatted` | string |  |

## Native endpoint

Through the native CallPage API, this operation is `GET /users/get` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.


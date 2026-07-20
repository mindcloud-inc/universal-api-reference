# Rachio Smart Hose Timer: Get Person

Retrieves person details from your Rachio account.

```
GET https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/get-person?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/get-person?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createDate": 1,
      "deleted": true,
      "devices": [
        {}
      ],
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createDate` | number | Creation timestamp in milliseconds. |
| `deleted` | boolean | Whether the person is deleted. |
| `devices` | array<object> | Associated devices. |
| `email` | string | Email address. |
| `fullName` | string | Full name. |
| `id` | string | Person id. |
| `username` | string | Rachio username. |

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `GET /public/person/:id` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.


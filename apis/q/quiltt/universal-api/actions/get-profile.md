# Quiltt: Get Profile



```
GET https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quiltt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/get-profile?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/get-profile?${params}`, {
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
| `profileId` | string | yes | Quiltt profile ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "at": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateOfBirth": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "names": {},
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `at` | date |  |
| `createdAt` | date |  |
| `dateOfBirth` | date |  |
| `email` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `names` | object |  |
| `phone` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Quiltt API, this operation is `GET /v1/profiles/:profileId` (base URL `https://api.quiltt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.


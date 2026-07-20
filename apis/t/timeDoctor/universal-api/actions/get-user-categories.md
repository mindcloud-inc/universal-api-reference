# Time Doctor: List User Categories

Retrieves user categories from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-user-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-user-categories?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-user-categories?${params}`, {
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
| `userId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entity": "string",
      "id": "string",
      "name": "Ava Chen",
      "scope": "string",
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity` | string |  |
| `id` | string |  |
| `name` | string |  |
| `scope` | string |  |
| `score` | number |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/categories/user/:userId` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-categories.md) for the provider-specific parameters and requirements.


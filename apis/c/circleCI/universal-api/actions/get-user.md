# CircleCI: Get User



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-user?connectionId=$CONNECTION_ID&id=6aac5412-4200-46cb-93ad-ec46ba27d19a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "6aac5412-4200-46cb-93ad-ec46ba27d19a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | The CircleCI user ID. Default: `6aac5412-4200-46cb-93ad-ec46ba27d19a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "login": "string",
      "name": "Ava Chen",
      "selectedEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `login` | string |  |
| `name` | string |  |
| `selectedEmail` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /user/:id` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.


# Jodoo: Get Member



```
GET https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-member?connectionId=$CONNECTION_ID&username=jdy-57q312f65pz7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "jdy-57q312f65pz7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-member?${params}`, {
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
| `username` | string | yes | Jodoo username to retrieve. Example: `jdy-57q312f65pz7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "departments": [
        1
      ],
      "name": "Ava Chen",
      "status": 1,
      "type": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departments[]` | number |  |
| `name` | string |  |
| `status` | number |  |
| `type` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST /corp/user/get` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member.md) for the provider-specific parameters and requirements.


# Status Hero: Get member



```
GET https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/get-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Status Hero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/get-member?connectionId=$CONNECTION_ID&id=5b73a1de-b26f-46fe-8f61-8355a2d9241b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "5b73a1de-b26f-46fe-8f61-8355a2d9241b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/get-member?${params}`, {
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
| `id` | string | yes | The Status Hero member ID or URL slug. Example: `5b73a1de-b26f-46fe-8f61-8355a2d9241b`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "absentDates": [
        "string"
      ],
      "id": "string",
      "role": "string",
      "slug": "string",
      "teamLead": true,
      "user": {},
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absentDates` | array<string> |  |
| `id` | string |  |
| `role` | string |  |
| `slug` | string |  |
| `teamLead` | boolean |  |
| `user` | object |  |
| `username` | string |  |

## Native endpoint

Through the native Status Hero API, this operation is `GET /members/:id` (base URL `https://service.statushero.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member.md) for the provider-specific parameters and requirements.


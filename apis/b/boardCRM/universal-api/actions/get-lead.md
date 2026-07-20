# BoardCRM: Get Lead

Retrieves a single lead from BoardCRM.

```
GET https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoardCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/get-lead?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/get-lead?${params}`, {
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
| `id` | number | yes | Lead ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "add_phone": "string",
      "created_at": "string",
      "email": "ava@example.com",
      "facebook": "string",
      "id": 1,
      "name": "Ava Chen",
      "note": "string",
      "organization": "string",
      "phone": "string",
      "position": "string",
      "skype": "string",
      "telegram": "string",
      "vk": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `add_phone` | string |  |
| `created_at` | string |  |
| `email` | string |  |
| `facebook` | string |  |
| `id` | number |  |
| `name` | string |  |
| `note` | string |  |
| `organization` | string |  |
| `phone` | string |  |
| `position` | string |  |
| `skype` | string |  |
| `telegram` | string |  |
| `vk` | string |  |
| `website` | string |  |

## Native endpoint

Through the native BoardCRM API, this operation is `POST /lead/get` (base URL `https://api.boardcrm.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.


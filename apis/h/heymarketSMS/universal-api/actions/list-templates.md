# Heymarket SMS: List Templates



```
GET https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-templates?${params}`, {
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
| `date` | string | no | Last updated cursor in RFC 3339 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "created": "2026-05-07T12:00:00.000Z",
      "creator_id": 1,
      "id": 1,
      "local_id": "string",
      "name": "Ava Chen",
      "op": "string",
      "rev": 1,
      "shared": true,
      "team_id": 1,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object |  |
| `created` | date |  |
| `creator_id` | number |  |
| `id` | number |  |
| `local_id` | string |  |
| `name` | string |  |
| `op` | string |  |
| `rev` | number |  |
| `shared` | boolean |  |
| `team_id` | number |  |
| `updated` | date |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `POST /v1/templates` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.


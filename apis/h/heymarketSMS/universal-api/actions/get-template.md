# Heymarket SMS: Get Template



```
GET https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-template?${params}`, {
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
| `templateId` | number | yes | Unique identifier of the template. |

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

Through the native Heymarket SMS API, this operation is `GET /v1/template/:id` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.


# Incontrol: Get Draft

Retrieves details for a draft from Incontrol.

```
GET https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Incontrol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-draft?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-draft?${params}`, {
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
| `id` | string | yes | The draft ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "createdLocal": "2026-05-07T12:00:00.000Z",
      "form": {},
      "id": "string",
      "incomplete": true,
      "loginLink": "https://example.com",
      "name": "Ava Chen",
      "reference": "string",
      "revision": true,
      "shared": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `createdLocal` | date |  |
| `form` | object |  |
| `id` | string |  |
| `incomplete` | boolean |  |
| `loginLink` | string |  |
| `name` | string |  |
| `reference` | string |  |
| `revision` | boolean |  |
| `shared` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Incontrol API, this operation is `GET /api/v1/draft/{{id}}` (base URL `https://portal.incontrol.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-draft.md) for the provider-specific parameters and requirements.


# Incontrol: Get Case

Retrieves details for a case from Incontrol.

```
GET https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-case
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Incontrol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-case?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-case?${params}`, {
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
| `id` | string | yes | The case ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {},
      "closed": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "deadline": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "group": {},
      "hasFiles": true,
      "hasNotes": true,
      "id": "string",
      "name": "Ava Chen",
      "number": 1,
      "organization": {},
      "originDocument": {},
      "priority": "string",
      "reporter": {},
      "status": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | object |  |
| `closed` | date |  |
| `created` | date |  |
| `deadline` | date |  |
| `description` | string |  |
| `group` | object |  |
| `hasFiles` | boolean |  |
| `hasNotes` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `number` | number |  |
| `organization` | object |  |
| `originDocument` | object |  |
| `priority` | string |  |
| `reporter` | object |  |
| `status` | string |  |
| `updated` | date |  |
| `user` | object |  |

## Native endpoint

Through the native Incontrol API, this operation is `GET /api/v1/case/{{id}}` (base URL `https://portal.incontrol.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-case.md) for the provider-specific parameters and requirements.


# Incontrol: Get Form

Retrieves details for a form from Incontrol.

```
GET https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Incontrol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-form?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-form?${params}`, {
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
| `id` | string | yes | The form ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "formTemplate": {},
      "groups": [
        {}
      ],
      "id": "string",
      "language": "string",
      "managed": true,
      "name": "Ava Chen",
      "organization": {},
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `formTemplate` | object |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `language` | string |  |
| `managed` | boolean |  |
| `name` | string |  |
| `organization` | object |  |
| `reference` | string |  |

## Native endpoint

Through the native Incontrol API, this operation is `GET /api/v1/form/{{id}}` (base URL `https://portal.incontrol.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.


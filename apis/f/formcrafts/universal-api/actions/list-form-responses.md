# Formcrafts: List Form Responses

Retrieves responses for a form from Formcrafts.

```
GET https://connect.mindcloud.co/v1/universal/formcrafts/latest/actions/list-form-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formcrafts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formcrafts/latest/actions/list-form-responses?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formcrafts/latest/actions/list-form-responses?${params}`, {
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
| `id` | string | yes | The Formcrafts form ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `before` | string | no | Return records created before this timestamp or resource marker, as supported by Formcrafts. Example: `2026-03-01T00:00:00Z`. |
| `after` | string | no | Return records created after this timestamp or resource marker, as supported by Formcrafts. Example: `2026-03-15T00:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "response": [
        {}
      ],
      "test": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visitor": {},
      "workflows": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | number |  |
| `response` | array<object> |  |
| `test` | boolean |  |
| `updatedAt` | date |  |
| `visitor` | object |  |
| `workflows` | array<object> |  |

## Native endpoint

Through the native Formcrafts API, this operation is `GET /forms/:id/responses` (base URL `https://api.formcrafts.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-responses.md) for the provider-specific parameters and requirements.


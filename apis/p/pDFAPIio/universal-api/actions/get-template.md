# PDF-API.io: Get Template

Retrieves a specific template from PDF-API.io.

```
GET https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-API.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/get-template?connectionId=$CONNECTION_ID&template=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/get-template?${params}`, {
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
| `template` | list<number> | yes | The unique identifier of the template you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "meta": {},
      "name": "Ava Chen",
      "teamId": 1,
      "teamName": "Ava Chen",
      "type": "string",
      "variables": [
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
| `createdAt` | date | The creation date of the template. |
| `id` | number | The unique identifier of the template. |
| `meta` | object | Additional metadata associated with the template. |
| `name` | string | The name of the template. |
| `teamId` | number | The unique identifier of the team that owns the template. |
| `teamName` | string | The name of the team that owns the template. |
| `type` | string | The type of the template, such as editor or html. |
| `variables` | array<object> | The variables defined for the template. |

## Native endpoint

Through the native PDF-API.io API, this operation is `GET /templates/:template` (base URL `https://pdf-api.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.


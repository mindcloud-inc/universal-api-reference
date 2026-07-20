# Reportei: Get Template

Retrieves a template from Reportei.

```
GET https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-template?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-template?${params}`, {
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
| `id` | number | yes | ID do template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "template": {
        "description": "string",
        "id": 1,
        "sections": [
          [
            {}
          ]
        ],
        "title": "string",
        "used_count": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `template.description` | string | Template description |
| `template.id` | number | Template identifier |
| `template.sections[]` | array<object> | Template sections |
| `template.title` | string | Template title |
| `template.used_count` | number | Times this template has been used |

## Native endpoint

Through the native Reportei API, this operation is `GET /templates/:id` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.


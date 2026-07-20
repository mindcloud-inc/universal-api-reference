# Sign.Plus: Get Template



```
GET https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign.Plus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/get-template?${params}`, {
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
| `templateId` | string | yes | ID of the template |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": {},
      "comment": "string",
      "created_at": 1,
      "documents": [
        {}
      ],
      "dynamic_fields": {},
      "expiration_delay": 1,
      "id": "string",
      "legality_level": "string",
      "name": "Ava Chen",
      "notification": {},
      "num_recipients": 1,
      "pages": 1,
      "signing_steps": [
        {}
      ],
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | object |  |
| `comment` | string |  |
| `created_at` | number |  |
| `documents` | array<object> |  |
| `dynamic_fields` | object |  |
| `expiration_delay` | number |  |
| `id` | string |  |
| `legality_level` | string |  |
| `name` | string |  |
| `notification` | object |  |
| `num_recipients` | number |  |
| `pages` | number |  |
| `signing_steps` | array<object> |  |
| `updated_at` | number |  |

## Native endpoint

Through the native Sign.Plus API, this operation is `GET /template/:template_id` (base URL `https://restapi.sign.plus/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.


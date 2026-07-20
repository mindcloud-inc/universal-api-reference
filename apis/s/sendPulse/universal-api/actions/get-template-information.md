# SendPulse: Get Template Information

Retrieves a template from SendPulse by ID.

```
GET https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-template-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-template-information?connectionId=$CONNECTION_ID&templateId=345678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "345678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-template-information?${params}`, {
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
| `templateId` | string | yes | The SendPulse template identifier. Example: `345678`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "category": "string",
      "category_info": [
        [
          "string"
        ]
      ],
      "created": "string",
      "id": "string",
      "is_structure": true,
      "lang": "string",
      "name": "Ava Chen",
      "name_slug": "Ava Chen",
      "owner": "string",
      "preview": "string",
      "real_id": 1,
      "tags": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `category` | string |  |
| `category_info[]` | array |  |
| `created` | string |  |
| `id` | string |  |
| `is_structure` | boolean |  |
| `lang` | string |  |
| `name` | string |  |
| `name_slug` | string |  |
| `owner` | string |  |
| `preview` | string |  |
| `real_id` | number |  |
| `tags[]` | array |  |

## Native endpoint

Through the native SendPulse API, this operation is `GET /template/:templateId` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-information.md) for the provider-specific parameters and requirements.


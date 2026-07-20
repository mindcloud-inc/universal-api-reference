# Picnie: Get Template

Retrieves a template and its fields from Picnie.

```
GET https://connect.mindcloud.co/v1/universal/picnie/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picnie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=2075" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "2075"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/picnie/latest/actions/get-template?${params}`, {
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
| `templateId` | string | yes | Picnie template identifier. Default: `2075`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completeObject": {
        "details": [
          {
            "imageUrl": "https://example.com",
            "name": "Ava Chen"
          }
        ],
        "name": "Ava Chen",
        "type": "string"
      },
      "error": true,
      "message": "string",
      "userObject": {
        "details": [
          {
            "imageUrl": "https://example.com",
            "name": "Ava Chen"
          }
        ],
        "templateId": 1,
        "templateName": "Ava Chen",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completeObject.details[].imageUrl` | string |  |
| `completeObject.details[].name` | string |  |
| `completeObject.name` | string |  |
| `completeObject.type` | string |  |
| `error` | boolean |  |
| `message` | string |  |
| `userObject.details[].imageUrl` | string |  |
| `userObject.details[].name` | string |  |
| `userObject.templateId` | number |  |
| `userObject.templateName` | string |  |
| `userObject.type` | string |  |

## Native endpoint

Through the native Picnie API, this operation is `POST /get-template` (base URL `https://picnie.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.


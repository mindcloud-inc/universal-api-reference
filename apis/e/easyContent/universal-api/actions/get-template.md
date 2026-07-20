# EasyContent: Get Template

Retrieves a template structure from EasyContent by ID.

```
GET https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/get-template?${params}`, {
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
| `templateId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "tabs": [
        {
          "fields": [
            {
              "guidelines": "string",
              "id": 1,
              "isEnabled": true,
              "isRequired": true,
              "position": 1,
              "recommendedLength": 1,
              "recommendedLengthUnits": "string",
              "title": "string",
              "type": "string"
            }
          ],
          "id": 1,
          "title": "string"
        }
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `tabs[].fields[].guidelines` | string |  |
| `tabs[].fields[].id` | number |  |
| `tabs[].fields[].isEnabled` | boolean |  |
| `tabs[].fields[].isRequired` | boolean |  |
| `tabs[].fields[].position` | number |  |
| `tabs[].fields[].recommendedLength` | number |  |
| `tabs[].fields[].recommendedLengthUnits` | string |  |
| `tabs[].fields[].title` | string |  |
| `tabs[].fields[].type` | string |  |
| `tabs[].id` | number |  |
| `tabs[].title` | string |  |
| `title` | string |  |

## Native endpoint

Through the native EasyContent API, this operation is `GET /v2/content/templates/:templateId` (base URL `https://easycontent.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.


# CraftMyPDF: Get template

Retrieves a template record from CraftMyPDF.

```
GET https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-template?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-template?${params}`, {
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
| `templateId` | string | no |  |
| `version` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "json": "string",
      "name": "Ava Chen",
      "status": "string",
      "templateId": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `json` | string |  |
| `name` | string |  |
| `status` | string |  |
| `templateId` | string |  |
| `version` | string |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `GET /get-template` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.


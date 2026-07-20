# Postmark: Get Template

Retrieves a template from Postmark.

```
GET https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-template?connectionId=$CONNECTION_ID&templateIdOrAlias=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateIdOrAlias": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-template?${params}`, {
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
| `templateIdOrAlias` | string | yes | The Postmark template ID or alias. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "Alias": "string",
      "AssociatedServerId": 1,
      "HtmlBody": "string",
      "LayoutTemplate": "string",
      "Name": "Ava Chen",
      "Subject": "string",
      "TemplateId": 1,
      "TemplateType": "string",
      "TextBody": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `Alias` | string |  |
| `AssociatedServerId` | number |  |
| `HtmlBody` | string |  |
| `LayoutTemplate` | string |  |
| `Name` | string |  |
| `Subject` | string |  |
| `TemplateId` | number |  |
| `TemplateType` | string |  |
| `TextBody` | string |  |

## Native endpoint

Through the native Postmark API, this operation is `GET /templates/:templateIdOrAlias` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.


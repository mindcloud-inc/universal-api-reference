# Postmark: Update Template

Updates a template in Postmark.

```
PUT https://connect.mindcloud.co/v1/universal/postmark/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateIdOrAlias": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmark/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateIdOrAlias": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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
      "LayoutTemplate": "string",
      "Name": "Ava Chen",
      "TemplateId": 1,
      "TemplateType": "string"
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
| `LayoutTemplate` | string |  |
| `Name` | string |  |
| `TemplateId` | number |  |
| `TemplateType` | string |  |

## Native endpoint

Through the native Postmark API, this operation is `PUT /templates/:templateIdOrAlias` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.


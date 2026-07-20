# CraftMyPDF: Create a new template

Creates a new template in CraftMyPDF.

```
POST https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-a-new-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-a-new-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/create-a-new-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes |  |
| `name` | string | no |  |
| `version` | string | no |  |
| `groupName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fromTemplateId": "string",
      "status": "string",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fromTemplateId` | string |  |
| `status` | string |  |
| `templateId` | string |  |

## Native endpoint

Through the native CraftMyPDF API, this operation is `POST /new-template-from` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-template.md) for the provider-specific parameters and requirements.


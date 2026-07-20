# Zoho Recruit: List Fields

Retrieves field metadata from Zoho Recruit.

```
GET https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-fields?connectionId=$CONNECTION_ID&moduleApiName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moduleApiName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-fields?${params}`, {
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
| `moduleApiName` | string | yes | The Zoho Recruit module API name whose fields you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiName": "Ava Chen",
      "customField": true,
      "dataType": "string",
      "defaultValue": "string",
      "displayLabel": "string",
      "fieldLabel": "string",
      "fieldReadOnly": true,
      "id": "string",
      "jsonType": "string",
      "length": 1,
      "lookup": {},
      "pickListValues": [
        {}
      ],
      "readOnly": true,
      "required": true,
      "systemMandatory": true,
      "viewType": {},
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiName` | string |  |
| `customField` | boolean |  |
| `dataType` | string |  |
| `defaultValue` | string |  |
| `displayLabel` | string |  |
| `fieldLabel` | string |  |
| `fieldReadOnly` | boolean |  |
| `id` | string |  |
| `jsonType` | string |  |
| `length` | number |  |
| `lookup` | object |  |
| `pickListValues` | array<object> |  |
| `readOnly` | boolean |  |
| `required` | boolean |  |
| `systemMandatory` | boolean |  |
| `viewType` | object |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Zoho Recruit API, this operation is `GET /settings/fields` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.


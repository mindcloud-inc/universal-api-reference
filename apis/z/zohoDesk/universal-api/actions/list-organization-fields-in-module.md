# Zoho Desk: List Organization Fields In Module



```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-organization-fields-in-module
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-organization-fields-in-module?connectionId=$CONNECTION_ID&module=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "module": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-organization-fields-in-module?${params}`, {
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
| `departmentId` | string | no | Optional department ID used when fetching module-specific organization fields. |
| `module` | string | yes | The Zoho Desk module name, such as tickets, contacts, or accounts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedValues": [
        {}
      ],
      "apiName": "Ava Chen",
      "displayLabel": "string",
      "i18NLabel": "string",
      "id": "string",
      "isCustomField": true,
      "isEncryptedField": true,
      "isMandatory": true,
      "lookup": {},
      "maxLength": 1,
      "name": "Ava Chen",
      "showToHelpCenter": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedValues` | array<object> |  |
| `apiName` | string |  |
| `displayLabel` | string |  |
| `i18NLabel` | string |  |
| `id` | string |  |
| `isCustomField` | boolean |  |
| `isEncryptedField` | boolean |  |
| `isMandatory` | boolean |  |
| `lookup` | object |  |
| `maxLength` | number |  |
| `name` | string |  |
| `showToHelpCenter` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET /organizationFields` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-fields-in-module.md) for the provider-specific parameters and requirements.


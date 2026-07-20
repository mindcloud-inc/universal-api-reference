# Zoho CRM: Get Modules

Retrieves available modules from Zoho CRM.

```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-modules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-modules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-modules?${params}`, {
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
| `status` | list | no | Module visibility status filter. One of: `not_included_in_conversion`, `scheduled_for_deletion`, `visible`, `visible_in_convert`. Example: `visible`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiName": "Ava Chen",
      "creatable": true,
      "editable": true,
      "id": "string",
      "moduleName": "Ava Chen",
      "singularLabel": "string",
      "status": "string",
      "viewable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiName` | string | Zoho CRM module API name. |
| `creatable` | boolean | Whether records can be created in the module. |
| `editable` | boolean | Whether records can be edited in the module. |
| `id` | string | Zoho CRM module ID. |
| `moduleName` | string | Zoho CRM internal module name. |
| `singularLabel` | string | Human-readable singular module label. |
| `status` | string | Module status. |
| `viewable` | boolean | Whether the module is viewable. |

## Native endpoint

Through the native Zoho CRM API, this operation is `GET /settings/modules` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-modules.md) for the provider-specific parameters and requirements.


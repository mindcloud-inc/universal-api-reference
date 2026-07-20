# Zoho CRM: Get Fields Metadata

Retrieves field metadata for a Zoho CRM module.

```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-fields-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-fields-metadata?connectionId=$CONNECTION_ID&moduleApiName=Leads" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moduleApiName": "Leads"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-fields-metadata?${params}`, {
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
| `moduleApiName` | string | yes | Zoho CRM module API name. Example: `Leads`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | list | no | Field metadata subset to return. One of: `all`, `unused`. Example: `all`. |
| `include` | string | no | Additional metadata sections to include. Example: `allowed_permissions_to_update`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiName": "Ava Chen",
      "customField": true,
      "dataType": "string",
      "displayLabel": "string",
      "fieldReadOnly": true,
      "id": "string",
      "jsonType": "string",
      "systemMandatory": true,
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiName` | string | Zoho CRM field API name. |
| `customField` | boolean | Whether the field is custom. |
| `dataType` | string | Zoho CRM field data type. |
| `displayLabel` | string | Human-readable field label. |
| `fieldReadOnly` | boolean | Whether the field is read-only in the API metadata. |
| `id` | string | Zoho CRM field ID. |
| `jsonType` | string | Underlying JSON type used by the field. |
| `systemMandatory` | boolean | Whether the field is system-mandatory. |
| `visible` | boolean | Whether the field is visible. |

## Native endpoint

Through the native Zoho CRM API, this operation is `GET /settings/fields` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fields-metadata.md) for the provider-specific parameters and requirements.


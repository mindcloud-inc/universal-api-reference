# Zoho Tables: List Fields

Retrieves all fields from Zoho Tables.

```
GET https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-fields?connectionId=$CONNECTION_ID&baseId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-fields?${params}`, {
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
| `baseId` | string | yes |  |
| `tableId` | string | yes |  |
| `viewId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultValue": "string",
      "fieldId": "string",
      "name": "Ava Chen",
      "type": "string",
      "typeComponents": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultValue` | string | Field default value when present. |
| `fieldId` | string | Zoho field identifier. |
| `name` | string | Field name. |
| `type` | string | Zoho field type code. |
| `typeComponents` | object | Type-specific field settings. |

## Native endpoint

Through the native Zoho Tables API, this operation is `GET /fields` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.


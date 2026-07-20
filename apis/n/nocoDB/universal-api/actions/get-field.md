# NocoDB: Get Field

Retrieves details for a field from NocoDB.

```
GET https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/get-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/get-field?connectionId=$CONNECTION_ID&baseId=string&fieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseId": "string",
  "fieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/get-field?${params}`, {
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
| `baseId` | string | yes | Base identifier. |
| `fieldId` | string | yes | Field identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "default_value": "string",
      "description": "string",
      "id": "string",
      "options": {},
      "system": true,
      "table_id": "string",
      "title": "string",
      "type": "string",
      "unique": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default_value` | string |  |
| `description` | string |  |
| `id` | string |  |
| `options` | object |  |
| `system` | boolean |  |
| `table_id` | string |  |
| `title` | string |  |
| `type` | string |  |
| `unique` | boolean |  |

## Native endpoint

Through the native NocoDB API, this operation is `GET /api/v3/meta/bases/:baseId/fields/:fieldId` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-field.md) for the provider-specific parameters and requirements.


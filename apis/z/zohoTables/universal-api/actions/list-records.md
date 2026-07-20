# Zoho Tables: List Records

Retrieves table records from Zoho Tables.

```
GET https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-records?connectionId=$CONNECTION_ID&baseId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-records?${params}`, {
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
| `recordId` | string | no |  |
| `count` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "displayData": {},
      "recordId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Record values keyed by field ID. |
| `displayData` | object | Display-friendly record values keyed by field ID. |
| `recordId` | string | Zoho record identifier. |

## Native endpoint

Through the native Zoho Tables API, this operation is `GET /records` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.


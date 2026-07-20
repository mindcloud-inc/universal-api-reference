# GrowthBook: Get a single Information Schema Table by id

Retrieves an information schema table from GrowthBook.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-information-schema-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-information-schema-table?connectionId=$CONNECTION_ID&tableId=table_1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "table_1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-information-schema-table?${params}`, {
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
| `tableId` | string | yes | The id of the information schema table Default: `table_1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "informationSchemaTable": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `informationSchemaTable` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /information-schema-tables/:tableId` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-information-schema-table.md) for the provider-specific parameters and requirements.


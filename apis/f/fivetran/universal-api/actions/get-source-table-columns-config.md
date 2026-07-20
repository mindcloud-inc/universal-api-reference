# Fivetran: Get Source Table Columns Config

Retrieves source table column configuration from Fivetran.

```
GET https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-source-table-columns-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-source-table-columns-config?connectionId=$CONNECTION_ID&connectionId=string&schema=string&table=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string",
  "schema": "string",
  "table": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-source-table-columns-config?${params}`, {
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
| `connectionId` | string | yes | The unique identifier for the connection within Fivetran. |
| `schema` | string | yes | The database schema name within the destination. |
| `table` | string | yes | The source table name from the connection schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "hashed": true,
      "isPrimaryKey": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `hashed` | boolean |  |
| `isPrimaryKey` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Fivetran API, this operation is `GET /connections/[:connectionId]/schemas/[:schema]/tables/[:table]/columns` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-source-table-columns-config.md) for the provider-specific parameters and requirements.


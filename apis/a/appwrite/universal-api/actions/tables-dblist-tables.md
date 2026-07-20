# Appwrite: List tables

Retrieves a list of tables from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dblist-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dblist-tables?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dblist-tables?${params}`, {
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
| `databaseId` | string | yes | Database ID. |
| `queries[]` | array<string> | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. You may filter on the following columns: name, enabled, rowSecurity Accepts multiple values as an array. |
| `search` | string | no | Search term to filter your list results. Max length: 256 chars. |
| `total` | boolean | no | When set to false, the total count returned will be 0 and will not be calculated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tables": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tables` | array<object> | List of tables. |
| `total` | number | Total number of tables that matched your query. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /tablesdb/{databaseId}/tables` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dblist-tables.md) for the provider-specific parameters and requirements.


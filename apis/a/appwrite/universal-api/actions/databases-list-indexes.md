# Appwrite: List indexes

Retrieves a list of indexes from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-list-indexes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-list-indexes?connectionId=$CONNECTION_ID&databaseId=string&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/databases-list-indexes?${params}`, {
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
| `collectionId` | string | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `queries[]` | array<string> | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. You may filter on the following attributes: key, type, status, attributes, error Accepts multiple values as an array. |
| `total` | boolean | no | When set to false, the total count returned will be 0 and will not be calculated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "indexes": [
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
| `indexes` | array<object> | List of indexes. |
| `total` | number | Total number of indexes that matched your query. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /databases/{databaseId}/collections/{collectionId}/indexes` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/databases-list-indexes.md) for the provider-specific parameters and requirements.


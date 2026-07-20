# Algolia: Retrieve a Record

Retrieves a record from an Algolia index.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-a-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-a-record?connectionId=$CONNECTION_ID&indexName=Ava%20Chen&objectID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen",
  "objectID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-a-record?${params}`, {
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
| `indexName` | string | yes | The name of the Algolia index. |
| `objectID` | string | yes | Unique identifier for the record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": "string",
      "category": "string",
      "color": "string",
      "isPublished": true,
      "name": "Ava Chen",
      "objectID": "string",
      "price": 1,
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | string |  |
| `category` | string |  |
| `color` | string |  |
| `isPublished` | boolean |  |
| `name` | string |  |
| `objectID` | string |  |
| `price` | number |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Algolia API, this operation is `GET /1/indexes/:indexName/:objectID` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-record.md) for the provider-specific parameters and requirements.


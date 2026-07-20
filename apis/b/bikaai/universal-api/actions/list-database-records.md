# Bika.ai: List Database Records

Retrieves database records from Bika.ai.

```
GET https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-database-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-database-records?connectionId=$CONNECTION_ID&spaceId=string&nodeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "nodeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-database-records?${params}`, {
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
| `spaceId` | string | yes | Bika.ai workspace/space ID. |
| `nodeId` | string | yes | Database node ID. In Bika.ai, the node ID is equivalent to the database ID for database resources. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "pageNum": 1,
        "pageSize": 1,
        "records": [
          {
            "createdAt": 1,
            "fields": {},
            "recordId": "string",
            "updatedAt": 1
          }
        ],
        "total": 1
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `data.pageNum` | number |  |
| `data.pageSize` | number |  |
| `data.records` | array<object> |  |
| `data.records[].createdAt` | number |  |
| `data.records[].fields` | object |  |
| `data.records[].recordId` | string |  |
| `data.records[].updatedAt` | number |  |
| `data.total` | number |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Bika.ai API, this operation is `GET /spaces/:spaceId/resources/databases/:nodeId/records` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-database-records.md) for the provider-specific parameters and requirements.


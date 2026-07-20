# Zixflow: Get List of Collection Records

Retrieves collection records from Zixflow.

```
GET https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-collection-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-collection-records?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-collection-records?${params}`, {
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
| `collectionId` | string | yes | Collection identifier. |
| `filter` | object | no | Filter object for collection-record query. |
| `sort[]` | array | no | Sort instructions for collection-record query. |
| `limit` | number | no | Maximum number of records to return. |
| `offset` | number | no | Number of records to skip. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array | Collection record rows returned by Zixflow. |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the collection-record query succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `POST /collection-records/:collectionId/query` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-of-collection-records.md) for the provider-specific parameters and requirements.


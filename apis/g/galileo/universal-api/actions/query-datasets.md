# Galileo: Query Datasets

Finds datasets in Galileo by query.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/query-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/query-datasets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/query-datasets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "datasets": [
        {
          "columnNames": [
            "Ava Chen"
          ],
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdByUser": {},
          "currentVersionIndex": 1,
          "draft": true,
          "id": "string",
          "name": "Ava Chen",
          "numRows": 1,
          "permissions": [
            {
              "action": "string",
              "allowed": true,
              "message": "string"
            }
          ],
          "projectCount": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "limit": 1,
      "nextStartingToken": 1,
      "paginated": true,
      "startingToken": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasets` | array<object> |  |
| `datasets[].columnNames` | array<string> |  |
| `datasets[].createdAt` | date |  |
| `datasets[].createdByUser` | object |  |
| `datasets[].currentVersionIndex` | number |  |
| `datasets[].draft` | boolean |  |
| `datasets[].id` | string |  |
| `datasets[].name` | string |  |
| `datasets[].numRows` | number |  |
| `datasets[].permissions` | array<object> |  |
| `datasets[].permissions[].action` | string |  |
| `datasets[].permissions[].allowed` | boolean |  |
| `datasets[].permissions[].message` | string |  |
| `datasets[].projectCount` | number |  |
| `datasets[].updatedAt` | date |  |
| `limit` | number |  |
| `nextStartingToken` | number |  |
| `paginated` | boolean |  |
| `startingToken` | number |  |

## Native endpoint

Through the native Galileo API, this operation is `POST /v2/datasets/query` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-datasets.md) for the provider-specific parameters and requirements.


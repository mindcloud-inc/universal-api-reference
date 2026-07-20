# AITable.ai: List Records

Retrieves records from a datasheet in AITable.ai.

```
GET https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-records?connectionId=$CONNECTION_ID&limit=25&offset=0&datasheetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "datasheetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-records?${params}`, {
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
| `datasheetId` | string | yes | AITable datasheet ID, for example dst0Yj5aNeoHldqvf6. |
| `viewId` | string | no | Optional view ID. When provided, AITable returns fields visible in that view. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldKey` | string | no | Use field names or field IDs when returning fields. AITable supports name or id. Default: `name`. |
| `maxRecords` | number | no | Optional maximum number of records to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageNum": 1,
      "pageSize": 1,
      "records": [
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
| `pageNum` | number | Current page number. |
| `pageSize` | number | Number of records returned per page. |
| `records` | array<object> | AITable records. |
| `total` | number | Total matching records. |

## Native endpoint

Through the native AITable.ai API, this operation is `GET /fusion/v1/datasheets/:datasheetId/records` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.


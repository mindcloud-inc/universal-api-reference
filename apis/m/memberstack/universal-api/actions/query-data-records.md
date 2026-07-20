# Memberstack: Query Data Records



```
GET https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/query-data-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memberstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/query-data-records?connectionId=$CONNECTION_ID&tableKey=string&query=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableKey": "string",
  "query": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/query-data-records?${params}`, {
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
| `tableKey` | string | yes | Target data table key. |
| `query` | object | yes | Query payload (filters, sorting, limits, and cursor fields). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "data": {},
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `data` | object |  |
| `id` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Memberstack API, this operation is `POST /v2/data-tables/:tableKey/records/query` (base URL `https://admin.memberstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-data-records.md) for the provider-specific parameters and requirements.


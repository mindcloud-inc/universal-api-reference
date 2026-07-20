# Quickbase: Get Reports for a Table

Retrieves all reports for a Quickbase table.

```
GET https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-reports-for-a-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-reports-for-a-table?connectionId=$CONNECTION_ID&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-reports-for-a-table?${params}`, {
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
| `tableId` | string | yes | The Quickbase table identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "ownerId": 1,
      "properties": {},
      "query": {},
      "type": "string",
      "usedCount": 1,
      "usedLast": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | The report description. |
| `id` | string | The report identifier. |
| `name` | string | The report name. |
| `ownerId` | number | The owner user ID when present. |
| `properties` | object | The report properties. |
| `query` | object | The configured report query. |
| `type` | string | The report type. |
| `usedCount` | number | How many times the report was used. |
| `usedLast` | date | When the report was last used. |

## Native endpoint

Through the native Quickbase API, this operation is `GET v1/reports` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reports-for-a-table.md) for the provider-specific parameters and requirements.


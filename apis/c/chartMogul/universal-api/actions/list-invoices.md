# ChartMogul: List Invoices

Retrieves invoices from ChartMogul.

```
GET https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartMogul `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-invoices?${params}`, {
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
      "collectionMethod": "string",
      "currency": "string",
      "customerExternalId": "string",
      "customerUuid": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "disabled": true,
      "disabledAt": "2026-05-07T12:00:00.000Z",
      "disabledBy": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "status": "string",
      "userCreated": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collectionMethod` | string |  |
| `currency` | string |  |
| `customerExternalId` | string |  |
| `customerUuid` | string |  |
| `date` | date |  |
| `disabled` | boolean |  |
| `disabledAt` | date |  |
| `disabledBy` | string |  |
| `dueDate` | date |  |
| `externalId` | string |  |
| `status` | string |  |
| `userCreated` | boolean |  |
| `uuid` | string |  |

## Native endpoint

Through the native ChartMogul API, this operation is `GET /invoices` (base URL `https://api.chartmogul.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.


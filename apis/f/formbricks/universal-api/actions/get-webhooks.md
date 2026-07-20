# Formbricks: Get Webhooks

Retrieves webhooks from Formbricks.

```
GET https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formbricks `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-webhooks?${params}`, {
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
| `limit` | number | no | Maximum number of webhooks to return. |
| `skip` | number | no | Number of webhooks to skip. |
| `sortBy` | string | no | Field to sort webhooks by. |
| `order` | string | no | Sort order. |
| `startDate` | date | no | Start date for filtering webhooks. |
| `endDate` | date | no | End date for filtering webhooks. |
| `filterDateField` | string | no | Date field to filter by. |
| `surveyIds` | string | no | Survey IDs to filter webhooks by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "environmentId": "string",
          "id": "string",
          "name": "Ava Chen",
          "source": "string",
          "surveyIds": [
            "string"
          ],
          "triggers": [
            "string"
          ],
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com"
        }
      ],
      "meta": {
        "limit": 1,
        "offset": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Webhooks returned by the management API. |
| `data[].createdAt` | date | Creation timestamp. |
| `data[].environmentId` | string | Environment ID associated with the webhook. |
| `data[].id` | string | Webhook ID. |
| `data[].name` | string | Webhook name. |
| `data[].source` | string | Webhook source type. |
| `data[].surveyIds` | array<string> | Survey IDs attached to the webhook. |
| `data[].triggers` | array<string> | Trigger event names. |
| `data[].updatedAt` | date | Last update timestamp. |
| `data[].url` | string | Destination URL for the webhook. |
| `meta` | object | Pagination metadata. |
| `meta.limit` | number | Applied page size. |
| `meta.offset` | number | Applied offset. |
| `meta.total` | number | Total number of matching webhooks. |

## Native endpoint

Through the native Formbricks API, this operation is `GET /management/webhooks` (base URL `https://app.formbricks.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-webhooks.md) for the provider-specific parameters and requirements.


# Avalara AvaTax: List Items By Company



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-items-by-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-items-by-company?connectionId=$CONNECTION_ID&limit=25&offset=0&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/list-items-by-company?${params}`, {
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
| `companyId` | number | yes | Avalara company ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "createdUserId": 1,
      "description": "string",
      "id": 1,
      "itemCode": "string",
      "itemStatus": [
        {}
      ],
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifiedUserId": 1,
      "taxCode": "string",
      "taxCodeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `createdDate` | date |  |
| `createdUserId` | number |  |
| `description` | string |  |
| `id` | number |  |
| `itemCode` | string |  |
| `itemStatus` | array<object> |  |
| `modifiedDate` | date |  |
| `modifiedUserId` | number |  |
| `taxCode` | string |  |
| `taxCodeId` | number |  |

## Native endpoint

Through the native Avalara AvaTax API, this operation is `GET companies/:companyId/items` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-items-by-company.md) for the provider-specific parameters and requirements.


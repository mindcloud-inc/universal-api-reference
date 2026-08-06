# Avalara AvaTax: Get Item



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-item?connectionId=$CONNECTION_ID&companyId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-item?${params}`, {
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
| `id` | number | yes | Avalara item ID. |

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

Through the native Avalara AvaTax API, this operation is `GET companies/:companyId/items/:id` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.


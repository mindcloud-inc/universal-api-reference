# RotaCloud: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-invoices?${params}`, {
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
| `dateFrom` | string | no |  |
| `dateTo` | string | no |  |
| `maxTotal` | number | no |  |
| `minTotal` | number | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountDue": 1,
      "currencyCode": "string",
      "date": "string",
      "deleted": true,
      "downloadLink": "https://example.com",
      "downloadLinkExpiresAt": "https://example.com",
      "dueDate": "string",
      "id": "string",
      "status": "string",
      "total": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountDue` | number |  |
| `currencyCode` | string |  |
| `date` | string |  |
| `deleted` | boolean |  |
| `downloadLink` | string |  |
| `downloadLinkExpiresAt` | string |  |
| `dueDate` | string |  |
| `id` | string |  |
| `status` | string |  |
| `total` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v2/invoices` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.


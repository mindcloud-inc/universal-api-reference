# Housecall Pro: Get Estimate



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-estimate?connectionId=$CONNECTION_ID&estimateId=csr_48c56f1d6e304fd3bd64069968d58d3b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "estimateId": "csr_48c56f1d6e304fd3bd64069968d58d3b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-estimate?${params}`, {
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
| `estimateId` | string | yes | Estimate identifier. Example: `csr_48c56f1d6e304fd3bd64069968d58d3b`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expand` | list<string> | no | Array of strings to expand response body. One of: `attachments`. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "assignedEmployees": [
        {}
      ],
      "companyId": "string",
      "companyName": "Ava Chen",
      "createdAt": "string",
      "customer": {},
      "estimateFields": {},
      "estimateNumber": "string",
      "id": "string",
      "leadSource": "string",
      "options": [
        {}
      ],
      "schedule": {},
      "updatedAt": "string",
      "workStatus": "string",
      "workTimestamps": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `assignedEmployees` | array<object> |  |
| `companyId` | string |  |
| `companyName` | string |  |
| `createdAt` | string |  |
| `customer` | object |  |
| `estimateFields` | object |  |
| `estimateNumber` | string |  |
| `id` | string |  |
| `leadSource` | string |  |
| `options` | array<object> |  |
| `schedule` | object |  |
| `updatedAt` | string |  |
| `workStatus` | string |  |
| `workTimestamps` | object |  |

## Native endpoint

Through the native Housecall Pro API, this operation is `GET /estimates/:estimate_id` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-estimate.md) for the provider-specific parameters and requirements.


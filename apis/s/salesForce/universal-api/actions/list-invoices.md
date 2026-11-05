# Salesforce: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforce `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/list-invoices?${params}`, {
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
| `status` | string | no | Match the current Status value exactly. This does not detect a transition into that status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "createdDate": "string",
      "lastModifiedDate": "string",
      "invoiceNumber": "string",
      "status": "string",
      "billingAccountId": "string",
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Provisional documentation-based field; runtime confirmation pending. |
| `createdDate` | string | Provisional documentation-based field; runtime confirmation pending. |
| `lastModifiedDate` | string | Provisional documentation-based field; runtime confirmation pending. |
| `invoiceNumber` | string | Provisional documentation-based field; runtime confirmation pending. |
| `status` | string | Provisional documentation-based field; runtime confirmation pending. |
| `billingAccountId` | string | Provisional documentation-based field; runtime confirmation pending. |
| `totalAmount` | number | Provisional documentation-based field; runtime confirmation pending. |

## Native endpoint

Through the native Salesforce API, this operation is `GET /services/data/v61.0/query` (base URL `https://{{credentials.companyDomainName}}.my.salesforce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.


# Salesforce: List Quote Line Items



```
GET https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/list-quote-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforce `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/list-quote-line-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/list-quote-line-items?${params}`, {
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
      "id": "string",
      "createdDate": "string",
      "lastModifiedDate": "string",
      "quoteId": "string",
      "quantity": 1,
      "unitPrice": 1
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
| `quoteId` | string | Provisional documentation-based field; runtime confirmation pending. |
| `quantity` | number | Provisional documentation-based field; runtime confirmation pending. |
| `unitPrice` | number | Provisional documentation-based field; runtime confirmation pending. |

## Native endpoint

Through the native Salesforce API, this operation is `GET /services/data/v61.0/query` (base URL `https://{{credentials.companyDomainName}}.my.salesforce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-quote-line-items.md) for the provider-specific parameters and requirements.


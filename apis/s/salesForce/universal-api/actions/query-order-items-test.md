# Salesforce: Query Order Items (test)



```
GET https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/query-order-items-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/query-order-items-test?connectionId=$CONNECTION_ID&where=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "where": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/query-order-items-test?${params}`, {
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
| `advancedOptions.orderBy` | list<string> | no |  |
| `where` | string | yes | This is a SOQL WHERE clause. Example: "AccountType != 'Vendor' AND CreatedDate != TODAY". Read more. |
| `advancedOptions.orderByDirection` | list<string> | no | Order Direction (ASC or DESC) - defaults is DESC. Default: `DESC`. |
| `select` | list<string> | no | Choose the fields to display in the response for this action. Accepts multiple values as an array. |
| `advancedOptions.limit` | number | no | Specify the limit for records returned in the response. The # of results. Example: 10. (Default: 2000) Default: `2000`. |
| `advancedOptions` | object | no | Specify additional query parameters and advanced SOQL syntax below. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesforce API returns.

## Native endpoint

Through the native Salesforce API, this operation is `GET services/data/v61.0/query` (base URL `https://{{credentials.companyDomainName}}.my.salesforce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-order-items-test.md) for the provider-specific parameters and requirements.


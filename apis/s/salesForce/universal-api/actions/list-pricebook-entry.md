# Salesforce: List Pricebook Entry



```
GET https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/list-pricebook-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/list-pricebook-entry?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/list-pricebook-entry?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesforce API returns.

## Native endpoint

Through the native Salesforce API, this operation is `GET /services/data/v56.0/query?q=SELECT+Id,+Product2Id,+Pricebook2Id,+Name,+ActivePriceAdjustmentQuantity,+IsActive,+IsArchived,+ProductCode,+ProductSellingModelId,+UseStandardPrice,+UnitPrice+FROM+PricebookEntry` (base URL `https://{{credentials.companyDomainName}}.my.salesforce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pricebook-entry.md) for the provider-specific parameters and requirements.


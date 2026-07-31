# Salesforce: Find Product Offer by Product Code



```
GET https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/find-product-by-product-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/find-product-by-product-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/find-product-by-product-code?${params}`, {
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
| `productcode` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesforce API returns.

## Native endpoint

Through the native Salesforce API, this operation is `GET services/data/v61.0/query?q=SELECT+Id,+ProductCode,+UPC__c,+%28SELECT+Quantity__c,+Consumed_Quantity__c,+id,+Vendor_ID__c,+Vendor_Offer__c+FROM Offers__r%29+FROM+Product2+WHERE+ProductCode+=+':productcode'` (base URL `https://{{credentials.companyDomainName}}.my.salesforce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-product-by-product-code.md) for the provider-specific parameters and requirements.


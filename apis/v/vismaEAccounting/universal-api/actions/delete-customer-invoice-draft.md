# Visma eAccounting: Delete Customer Invoice Draft

Deletes an existing customer invoice draft from Visma eAccounting.

```
DELETE https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/delete-customer-invoice-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/delete-customer-invoice-draft?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/delete-customer-invoice-draft?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Visma eAccounting API returns.

## Native endpoint

Through the native Visma eAccounting API, this operation is `DELETE /customerinvoicedrafts/{customerInvoiceDraftId}` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer-invoice-draft.md) for the provider-specific parameters and requirements.


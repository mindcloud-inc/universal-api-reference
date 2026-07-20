# PhantomBuster: Get Organization CRM Resources

Retrieves organization CRM resources from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization-crm-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization-crm-resources?connectionId=$CONNECTION_ID&resourceType=account_info" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceType": "account_info"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization-crm-resources?${params}`, {
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
| `resourceType` | list | yes | Type of CRM resource to fetch. Allowed values: account_info, contact_lists, contact_properties. One of: `account_info`, `contact_lists`, `contact_properties`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PhantomBuster API returns.

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /orgs/fetch-crm-resources` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-crm-resources.md) for the provider-specific parameters and requirements.


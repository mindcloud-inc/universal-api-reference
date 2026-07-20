# GoDaddy CRM: Retrieve Domain Purchase Agreements

Retrieves domain purchase agreements from GoDaddy.

```
GET https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/retrieve-domain-purchase-agreements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/retrieve-domain-purchase-agreements?connectionId=$CONNECTION_ID&tlds%5B%5D=string&privacy=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tlds[]": "string",
  "privacy": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/retrieve-domain-purchase-agreements?${params}`, {
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
| `tlds[]` | array<string> | yes | List of TLDs whose legal agreements should be retrieved. |
| `privacy` | boolean | yes | Whether privacy has been requested. |
| `forTransfer` | boolean | no | Whether a domain transfer has been requested. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `GET /v1/domains/agreements` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-domain-purchase-agreements.md) for the provider-specific parameters and requirements.


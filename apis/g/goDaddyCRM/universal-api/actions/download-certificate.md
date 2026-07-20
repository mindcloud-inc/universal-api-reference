# GoDaddy CRM: Download Certificate

Downloads a customer certificate from GoDaddy.

```
GET https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/download-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/download-certificate?connectionId=$CONNECTION_ID&entitlementId=dummy-entitlement-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entitlementId": "dummy-entitlement-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/download-certificate?${params}`, {
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
| `entitlementId` | string | yes | Required entitlement identifier to download Example: `dummy-entitlement-id`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `GET /v2/certificates/download` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-certificate.md) for the provider-specific parameters and requirements.


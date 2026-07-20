# GoDaddy CRM: Check Domain Availability

Checks domain availability with the GoDaddy API.

```
GET https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/check-domain-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/check-domain-availability?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/check-domain-availability?${params}`, {
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
| `domain` | string | yes | Domain name whose availability is to be checked. |
| `checkType` | string | no | Optimize for time (FAST) or accuracy (FULL). Default: `FAST`. |
| `forTransfer` | boolean | no | Whether to include domains available for transfer. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `GET /v1/domains/available` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-domain-availability.md) for the provider-specific parameters and requirements.


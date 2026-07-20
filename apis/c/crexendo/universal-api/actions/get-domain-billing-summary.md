# Crexendo: Get Domain Billing Summary

Retrieves a domain billing summary from Crexendo.

```
GET https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-domain-billing-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crexendo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-domain-billing-summary?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-domain-billing-summary?${params}`, {
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
| `domain` | string | yes | Domain identifier, for example apps.mindcloud.co. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count-call-queues": 1,
      "count-phone-numbers": 1,
      "count-users-total": 1,
      "description": "string",
      "domain": "string",
      "limits-max-active-calls-total": 1,
      "reseller": "string",
      "sms-sent-this-month": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count-call-queues` | number |  |
| `count-phone-numbers` | number |  |
| `count-users-total` | number |  |
| `description` | string |  |
| `domain` | string |  |
| `limits-max-active-calls-total` | number |  |
| `reseller` | string |  |
| `sms-sent-this-month` | number |  |

## Native endpoint

Through the native Crexendo API, this operation is `GET /domains/:domain/billing` (base URL `https://ns-api.com/ns-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-billing-summary.md) for the provider-specific parameters and requirements.


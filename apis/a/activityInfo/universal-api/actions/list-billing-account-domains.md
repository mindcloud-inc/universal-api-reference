# ActivityInfo: List Billing Account Domains

Retrieves domains for an ActivityInfo billing account.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-billing-account-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-billing-account-domains?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-billing-account-domains?${params}`, {
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
| `accountId` | string | yes | ActivityInfo billing account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryStatus": "string",
      "domain": "string",
      "idp": "string",
      "userCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryStatus` | string | Email delivery status. |
| `domain` | string | Email domain. |
| `idp` | string | Linked identity provider, if present. |
| `userCount` | number | Count of user accounts on this domain. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/billingAccounts/:accountId/domains` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-billing-account-domains.md) for the provider-specific parameters and requirements.


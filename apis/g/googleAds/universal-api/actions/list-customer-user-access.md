# Google Ads: List Customer User Access

Retrieves customer user access from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-user-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-user-access?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20customer_user_access.user_id%2C%20customer_user_access.email_address%20FROM%20customer_user_access" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT customer_user_access.user_id, customer_user_access.email_address FROM customer_user_access"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-user-access?${params}`, {
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
| `customerId` | list<string> | yes | Customer ID to query (without dashes). Example: `1234567890`. |
| `query` | string | yes | GAQL query for customer_user_access visibility. Default: `SELECT customer_user_access.user_id, customer_user_access.email_address, customer_user_access.access_role, customer_user_access.inviter_user_email_address FROM customer_user_access`. Example: `SELECT customer_user_access.user_id, customer_user_access.email_address FROM customer_user_access`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerUserAccess": {
        "accessRole": "string",
        "emailAddress": "ava@example.com",
        "inviterUserEmailAddress": "ava@example.com",
        "resourceName": "Ava Chen",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerUserAccess.accessRole` | string |  |
| `customerUserAccess.emailAddress` | string |  |
| `customerUserAccess.inviterUserEmailAddress` | string |  |
| `customerUserAccess.resourceName` | string |  |
| `customerUserAccess.userId` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-user-access.md) for the provider-specific parameters and requirements.


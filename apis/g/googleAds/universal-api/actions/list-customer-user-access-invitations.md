# Google Ads: List Customer User Access Invitations

Retrieves customer user access invitations from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-user-access-invitations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-user-access-invitations?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20customer_user_access_invitation.invitation_id%2C%20customer_user_access_invitation.email_address%20FROM%20customer_user_access_invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT customer_user_access_invitation.invitation_id, customer_user_access_invitation.email_address FROM customer_user_access_invitation"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-user-access-invitations?${params}`, {
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
| `query` | string | yes | GAQL query for customer_user_access_invitation visibility. Default: `SELECT customer_user_access_invitation.invitation_id, customer_user_access_invitation.email_address, customer_user_access_invitation.access_role, customer_user_access_invitation.creation_date_time FROM customer_user_access_invitation`. Example: `SELECT customer_user_access_invitation.invitation_id, customer_user_access_invitation.email_address FROM customer_user_access_invitation`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldMask": "string",
      "queryResourceConsumption": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldMask` | string |  |
| `queryResourceConsumption` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-user-access-invitations.md) for the provider-specific parameters and requirements.


# Recommand: Delete Company Notification Email Address

Deletes a company notification email address from Recommand.

```
DELETE https://connect.mindcloud.co/v1/universal/recommand/latest/actions/delete-company-notification-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/delete-company-notification-email-address?connectionId=$CONNECTION_ID&companyid=string&notificationemailaddressid=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyid": "string",
  "notificationemailaddressid": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/delete-company-notification-email-address?${params}`, {
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
| `companyid` | string | yes | companyId parameter. |
| `notificationemailaddressid` | string | yes | notificationEmailAddressId parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `DELETE /api/v1/companies/:companyId/notification-email-addresses/:notificationEmailAddressId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-company-notification-email-address.md) for the provider-specific parameters and requirements.


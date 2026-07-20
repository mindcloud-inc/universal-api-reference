# Outseta: Add New Person to Existing Account

Adds a new person to an existing account in Outseta.

```
POST https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-new-person-to-existing-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-new-person-to-existing-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountUid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-new-person-to-existing-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountUid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountUid` | string | yes |  |
| `sendWelcomeEmail` | boolean | no |  |
| `person.email` | string | no |  |
| `person.firstName` | string | no |  |
| `person.lastName` | string | no |  |
| `isPrimary` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Account": {
        "AccountStage": 1,
        "BillingAddress": "string",
        "ClientIdentifier": "string",
        "Created": "string",
        "MailingAddress": "string",
        "Name": "Ava Chen",
        "PaymentInformation": "string",
        "PersonAccount": "string",
        "Subscriptions": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "Created": "string",
      "IsPrimary": true,
      "Person": {
        "Created": "string",
        "Email": "ava@example.com",
        "EmailBounceDateTime": "ava@example.com",
        "EmailLastDeliveredDateTime": "ava@example.com",
        "EmailSpamDateTime": "ava@example.com",
        "EmailUnsubscribeDateTime": "ava@example.com",
        "FirstName": "Ava",
        "FullName": "Ava Chen",
        "LastName": "Chen",
        "MailingAddress": "string",
        "PersonAccount": "string",
        "PhoneMobile": "string",
        "PhoneWork": "string",
        "Timezone": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "Uid": "string",
      "Updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Account.AccountStage` | number |  |
| `Account.BillingAddress` | string |  |
| `Account.ClientIdentifier` | string |  |
| `Account.Created` | string |  |
| `Account.MailingAddress` | string |  |
| `Account.Name` | string |  |
| `Account.PaymentInformation` | string |  |
| `Account.PersonAccount` | string |  |
| `Account.Subscriptions` | string |  |
| `Account.Uid` | string |  |
| `Account.Updated` | string |  |
| `Created` | string |  |
| `IsPrimary` | boolean |  |
| `Person.Created` | string |  |
| `Person.Email` | string |  |
| `Person.EmailBounceDateTime` | string |  |
| `Person.EmailLastDeliveredDateTime` | string |  |
| `Person.EmailSpamDateTime` | string |  |
| `Person.EmailUnsubscribeDateTime` | string |  |
| `Person.FirstName` | string |  |
| `Person.FullName` | string |  |
| `Person.LastName` | string |  |
| `Person.MailingAddress` | string |  |
| `Person.PersonAccount` | string |  |
| `Person.PhoneMobile` | string |  |
| `Person.PhoneWork` | string |  |
| `Person.Timezone` | string |  |
| `Person.Uid` | string |  |
| `Person.Updated` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `POST /crm/accounts/:accountUid/memberships` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-new-person-to-existing-account.md) for the provider-specific parameters and requirements.


# Outseta: Add Account with New Person

Creates an account with a new person in Outseta.

```
POST https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-account-with-new-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-account-with-new-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-account-with-new-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendConfirmationEmail` | boolean | no |  |
| `name` | string | no |  |
| `accountStage` | string | no |  |
| `mailingAddress.addressLine1` | string | no |  |
| `mailingAddress.addressLine2` | string | no |  |
| `mailingAddress.city` | string | no |  |
| `mailingAddress.state` | string | no |  |
| `mailingAddress.postalCode` | string | no |  |
| `billingAddress.addressLine1` | string | no |  |
| `billingAddress.addressLine2` | string | no |  |
| `billingAddress.city` | string | no |  |
| `billingAddress.state` | string | no |  |
| `billingAddress.postalCode` | string | no |  |
| `personAccount[].person.email` | string | no |  |
| `personAccount[].person.firstName` | string | no |  |
| `personAccount[].person.lastName` | string | no |  |
| `personAccount[].isPrimary` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AccountStage": 1,
      "BillingAddress": {
        "AddressLine1": "string",
        "AddressLine2": "string",
        "AddressLine3": "string",
        "City": "string",
        "Created": "string",
        "PostalCode": "string",
        "State": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "ClientIdentifier": "string",
      "Created": "string",
      "MailingAddress": {
        "AddressLine1": "string",
        "AddressLine2": "string",
        "AddressLine3": "string",
        "City": "string",
        "Created": "string",
        "PostalCode": "string",
        "State": "string",
        "Uid": "string",
        "Updated": "string"
      },
      "Name": "Ava Chen",
      "PaymentInformation": "string",
      "PersonAccount": [
        {
          "Account": "string",
          "Created": "string",
          "IsPrimary": true,
          "Person": "string",
          "Uid": "string",
          "Updated": "string"
        }
      ],
      "Subscriptions": [
        "string"
      ],
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
| `AccountStage` | number |  |
| `BillingAddress.AddressLine1` | string |  |
| `BillingAddress.AddressLine2` | string |  |
| `BillingAddress.AddressLine3` | string |  |
| `BillingAddress.City` | string |  |
| `BillingAddress.Created` | string |  |
| `BillingAddress.PostalCode` | string |  |
| `BillingAddress.State` | string |  |
| `BillingAddress.Uid` | string |  |
| `BillingAddress.Updated` | string |  |
| `ClientIdentifier` | string |  |
| `Created` | string |  |
| `MailingAddress.AddressLine1` | string |  |
| `MailingAddress.AddressLine2` | string |  |
| `MailingAddress.AddressLine3` | string |  |
| `MailingAddress.City` | string |  |
| `MailingAddress.Created` | string |  |
| `MailingAddress.PostalCode` | string |  |
| `MailingAddress.State` | string |  |
| `MailingAddress.Uid` | string |  |
| `MailingAddress.Updated` | string |  |
| `Name` | string |  |
| `PaymentInformation` | string |  |
| `PersonAccount` | array<object> |  |
| `PersonAccount[].Account` | string |  |
| `PersonAccount[].Created` | string |  |
| `PersonAccount[].IsPrimary` | boolean |  |
| `PersonAccount[].Person` | string |  |
| `PersonAccount[].Uid` | string |  |
| `PersonAccount[].Updated` | string |  |
| `Subscriptions` | array<string> |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `POST /crm/accounts` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-account-with-new-person.md) for the provider-specific parameters and requirements.


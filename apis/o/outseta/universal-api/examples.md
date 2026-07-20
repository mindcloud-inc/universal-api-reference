# Outseta Universal API Examples

These examples use the MindCloud API key and Outseta connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves a list of accounts from Outseta.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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
        {
          "Account": "string",
          "BillingRenewalTerm": 1,
          "Created": "string",
          "EndDate": "string",
          "IsPlanUpgradeRequired": true,
          "NewRequiredQuantity": "string",
          "Plan": "string",
          "PlanUpgradeRequiredMessage": "string",
          "Quantity": "string",
          "RenewalDate": "string",
          "StartDate": "string",
          "SubscriptionAddOns": "string",
          "Uid": "string",
          "Updated": "string"
        }
      ],
      "Uid": "string",
      "Updated": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/outseta/latest/actions/list-accounts).

## Add Account with Existing Person

Creates an account with an existing person in Outseta.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-account-with-existing-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-account-with-existing-person', {
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

Example response:

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

See the full [Add Account with Existing Person action reference](actions/add-account-with-existing-person.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/outseta/latest/actions/add-account-with-existing-person).

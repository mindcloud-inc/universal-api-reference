# Outseta: Add Person

Creates a new person in Outseta.

```
POST https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/add-person', {
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
| `email` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `mailingAddress.addressLine1` | string | no |  |
| `mailingAddress.addressLine2` | string | no |  |
| `mailingAddress.addressLine3` | string | no |  |
| `mailingAddress.city` | string | no |  |
| `mailingAddress.state` | string | no |  |
| `mailingAddress.postalCode` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Created": "string",
      "Email": "ava@example.com",
      "EmailBounceDateTime": "ava@example.com",
      "EmailLastDeliveredDateTime": "ava@example.com",
      "EmailSpamDateTime": "ava@example.com",
      "EmailUnsubscribeDateTime": "ava@example.com",
      "FirstName": "Ava",
      "FullName": "Ava Chen",
      "LastName": "Chen",
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
      "PersonAccount": [
        "string"
      ],
      "PhoneMobile": "string",
      "PhoneWork": "string",
      "Timezone": "string",
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
| `Created` | string |  |
| `Email` | string |  |
| `EmailBounceDateTime` | string |  |
| `EmailLastDeliveredDateTime` | string |  |
| `EmailSpamDateTime` | string |  |
| `EmailUnsubscribeDateTime` | string |  |
| `FirstName` | string |  |
| `FullName` | string |  |
| `LastName` | string |  |
| `MailingAddress.AddressLine1` | string |  |
| `MailingAddress.AddressLine2` | string |  |
| `MailingAddress.AddressLine3` | string |  |
| `MailingAddress.City` | string |  |
| `MailingAddress.Created` | string |  |
| `MailingAddress.PostalCode` | string |  |
| `MailingAddress.State` | string |  |
| `MailingAddress.Uid` | string |  |
| `MailingAddress.Updated` | string |  |
| `PersonAccount` | array<string> |  |
| `PhoneMobile` | string |  |
| `PhoneWork` | string |  |
| `Timezone` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `POST /crm/people` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-person.md) for the provider-specific parameters and requirements.


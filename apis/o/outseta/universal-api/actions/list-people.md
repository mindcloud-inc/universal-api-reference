# Outseta: List People

Retrieves a list of people from Outseta.

```
GET https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outseta/latest/actions/list-people?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
| `PhoneMobile` | string |  |
| `PhoneWork` | string |  |
| `Timezone` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `GET /crm/people` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.


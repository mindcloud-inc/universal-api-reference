# Outseta: Get Person

Retrieves a person from Outseta.

```
GET https://connect.mindcloud.co/v1/universal/outseta/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/get-person?connectionId=$CONNECTION_ID&personUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outseta/latest/actions/get-person?${params}`, {
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
| `personUid` | string | yes |  |

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
      "MailingAddress": "string",
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
| `MailingAddress` | string |  |
| `PersonAccount` | array<string> |  |
| `PhoneMobile` | string |  |
| `PhoneWork` | string |  |
| `Timezone` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `GET /crm/people/:personUid` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.


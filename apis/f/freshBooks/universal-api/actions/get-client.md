# FreshBooks: Get Client

Retrieves a client from FreshBooks for an account.

```
GET https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreshBooks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-client?connectionId=$CONNECTION_ID&accountId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-client?${params}`, {
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
| `accountId` | string | yes | FreshBooks accounting account ID. |
| `userId` | string | yes | FreshBooks client user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountingSystemid": "string",
      "allowEmailIncludePdf": true,
      "allowLateFees": true,
      "allowLateNotifications": true,
      "busPhone": "string",
      "currencyCode": "string",
      "email": "ava@example.com",
      "exceedsClientLimit": 1,
      "fax": "string",
      "fname": "Ava Chen",
      "homePhone": "string",
      "id": 1,
      "language": "string",
      "level": 1,
      "lname": "Ava Chen",
      "mobPhone": "string",
      "note": "string",
      "notified": true,
      "numLogins": 1,
      "organization": "string",
      "pCity": "string",
      "pCode": "string",
      "pCountry": "string",
      "pProvince": "string",
      "prefEmail": true,
      "prefGmail": true,
      "pStreet": "string",
      "pStreet2": "string",
      "role": "string",
      "sCity": "string",
      "sCode": "string",
      "sCountry": "string",
      "signupDate": "string",
      "sProvince": "string",
      "sStreet": "string",
      "sStreet2": "string",
      "updated": "string",
      "userid": 1,
      "username": "Ava Chen",
      "uuid": "string",
      "visState": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountingSystemid` | string |  |
| `allowEmailIncludePdf` | boolean |  |
| `allowLateFees` | boolean |  |
| `allowLateNotifications` | boolean |  |
| `busPhone` | string |  |
| `currencyCode` | string |  |
| `email` | string |  |
| `exceedsClientLimit` | number |  |
| `fax` | string |  |
| `fname` | string |  |
| `homePhone` | string |  |
| `id` | number |  |
| `language` | string |  |
| `level` | number |  |
| `lname` | string |  |
| `mobPhone` | string |  |
| `note` | string |  |
| `notified` | boolean |  |
| `numLogins` | number |  |
| `organization` | string |  |
| `pCity` | string |  |
| `pCode` | string |  |
| `pCountry` | string |  |
| `pProvince` | string |  |
| `prefEmail` | boolean |  |
| `prefGmail` | boolean |  |
| `pStreet` | string |  |
| `pStreet2` | string |  |
| `role` | string |  |
| `sCity` | string |  |
| `sCode` | string |  |
| `sCountry` | string |  |
| `signupDate` | string |  |
| `sProvince` | string |  |
| `sStreet` | string |  |
| `sStreet2` | string |  |
| `updated` | string |  |
| `userid` | number |  |
| `username` | string |  |
| `uuid` | string |  |
| `visState` | number |  |

## Native endpoint

Through the native FreshBooks API, this operation is `GET /accounting/account/:accountId/users/clients/:userId` (base URL `https://api.freshbooks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.


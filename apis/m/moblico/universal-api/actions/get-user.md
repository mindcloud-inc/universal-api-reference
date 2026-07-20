# Moblico: Get User



```
GET https://connect.mindcloud.co/v1/universal/moblico/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moblico `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moblico/latest/actions/get-user?connectionId=$CONNECTION_ID&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moblico/latest/actions/get-user?${params}`, {
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
| `username` | string | yes | Moblico username to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "address2": "string",
      "age": 1,
      "attributes": {},
      "city": "string",
      "companyAccountNumber": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "createDate": "2026-05-07T12:00:00.000Z",
      "dateOfBirth": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalId": "string",
      "firstName": "Ava",
      "gender": "string",
      "id": 1,
      "lastName": "Chen",
      "lastUpdateDate": "2026-05-07T12:00:00.000Z",
      "locale": "string",
      "locationId": "string",
      "merchantId": "string",
      "nickName": "Ava Chen",
      "optinBusinessEmail": true,
      "optinBusinessPhone": true,
      "optinEmail": true,
      "optinPhone": true,
      "phone": "string",
      "postalCode": "string",
      "stateOrProvince": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string | Address line 1. |
| `address2` | string | Address line 2. |
| `age` | number | Age. |
| `attributes` | object | Additional Moblico user attributes. |
| `city` | string | City. |
| `companyAccountNumber` | string | Company account number. |
| `companyName` | string | Company name. |
| `country` | string | Country. |
| `createDate` | date | Creation timestamp. |
| `dateOfBirth` | date | Date of birth. |
| `email` | string | Email address. |
| `externalId` | string | External user identifier. |
| `firstName` | string | First name. |
| `gender` | string | Gender value. |
| `id` | number | Moblico user ID. |
| `lastName` | string | Last name. |
| `lastUpdateDate` | date | Last update timestamp. |
| `locale` | string | Locale. |
| `locationId` | string | Location ID. |
| `merchantId` | string | Merchant ID. |
| `nickName` | string | Nickname. |
| `optinBusinessEmail` | boolean | Business email opt-in flag. |
| `optinBusinessPhone` | boolean | Business phone opt-in flag. |
| `optinEmail` | boolean | Email opt-in flag. |
| `optinPhone` | boolean | Phone opt-in flag. |
| `phone` | string | Phone number. |
| `postalCode` | string | Postal code. |
| `stateOrProvince` | string | State or province. |
| `username` | string | Moblico username. |

## Native endpoint

Through the native Moblico API, this operation is `GET /users/:username` (base URL `https://moblico.net/services/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.


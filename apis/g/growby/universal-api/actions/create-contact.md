# Growby: Create Contact

Creates a new contact in Growby.

```
POST https://connect.mindcloud.co/v1/universal/growby/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Growby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growby/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "nationalNumber": "string",
  "countryCode": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growby/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "nationalNumber": "string",
    "countryCode": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Contact first name. Required by Growby. |
| `nationalNumber` | string | yes | Phone number without the country code. Required by Growby. |
| `countryCode` | number | yes | Numeric country code for the contact phone number. Required by Growby. Default: `1`. |
| `lastName` | string | no | Contact last name. |
| `emailId` | string | no | Contact email address. |
| `source` | string | no | Lead source or origin label for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "response": "string",
      "statuscode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Created contact payload returned by Growby. |
| `response` | string | Growby result text. |
| `statuscode` | number | HTTP-like status code returned by Growby. |

## Native endpoint

Through the native Growby API, this operation is `POST /devapi/AddContact` (base URL `https://api.growby.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.


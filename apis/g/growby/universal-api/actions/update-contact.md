# Growby: Update Contact

Updates an existing contact in Growby.

```
PUT https://connect.mindcloud.co/v1/universal/growby/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Growby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growby/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "firstName": "Ava",
  "nationalNumber": "string",
  "countryCode": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growby/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
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
| `id` | number | yes | Growby contact id to update. |
| `firstName` | string | yes | Updated first name. Required by Growby. |
| `nationalNumber` | string | yes | Updated phone number without country code. Required by Growby. |
| `countryCode` | number | yes | Updated numeric country code. Required by Growby. Default: `1`. |
| `lastName` | string | no | Updated last name. |
| `emailId` | string | no | Updated email address. |
| `source` | string | no | Updated lead source or origin label. |

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
| `data` | object | Updated contact payload returned by Growby. |
| `response` | string | Growby result text. |
| `statuscode` | number | HTTP-like status code returned by Growby. |

## Native endpoint

Through the native Growby API, this operation is `PUT /devapi/contact/:id` (base URL `https://api.growby.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.


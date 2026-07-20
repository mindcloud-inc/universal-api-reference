# Leverly: Create Call



```
POST https://connect.mindcloud.co/v1/universal/leverly/latest/actions/create-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leverly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leverly/latest/actions/create-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "phone1": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leverly/latest/actions/create-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "phone1": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address1` | string | no | Lead's address. |
| `area` | string | no | Lead's area of interest. |
| `callDelay` | number | no | Delay before the initial call in seconds. |
| `callerId` | string | no | Caller ID to display on leg 1 of the call. |
| `city` | string | no | Lead's city. |
| `comments` | string | no | Lead comments. |
| `companyName` | string | no | Lead's company name. |
| `email` | string | no | Lead's email address. |
| `keyword` | string | no | Lead's keyword. |
| `lastName` | string | no | Lead's last name. |
| `leadSource` | string | no | Lead's source. |
| `location` | string | no | Lead's location. |
| `phone2` | string | no | Lead's second phone number. |
| `phone3` | string | no | Lead's third phone number. |
| `phone4` | string | no | Lead's fourth phone number. |
| `program` | string | no | Lead's program of interest. |
| `repPhone` | string | no | Representative phone number. Separate multiple numbers with commas. |
| `routingType` | number | no | 1 = Step ringing, 2 = Round robin, 3 = Simultaneous. |
| `state` | string | no | Lead's state. |
| `vendorLeadId` | string | no | Vendor lead identifier used to reconcile and stop a submitted call later. |
| `zip` | string | no | Lead's ZIP code. |
| `firstName` | string | yes | Lead's first name. |
| `phone1` | string | yes | Lead's primary phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inquiryId": 1,
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inquiryId` | number | Leverly inquiry identifier for the submitted lead. |
| `message` | string | Human-readable result message returned by Leverly. |
| `status` | string | Result status returned by Leverly. |

## Native endpoint

Through the native Leverly API, this operation is `POST /ingestor/process` (base URL `https://app.leverly.com/main`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-call.md) for the provider-specific parameters and requirements.


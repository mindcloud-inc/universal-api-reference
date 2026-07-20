# EchtPost Postcards: Create Card From Contact Data

Creates a postcard from contact data in EchtPost Postcards.

```
POST https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/create-card-from-contact-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EchtPost Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/create-card-from-contact-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "city": "string",
  "countryCode": "string",
  "deliverAt": "2026-05-07T12:00:00.000Z",
  "firstName": "Ava",
  "lastName": "Chen",
  "street": "string",
  "templateId": 1,
  "zip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/create-card-from-contact-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "city": "string",
    "countryCode": "string",
    "deliverAt": "2026-05-07T12:00:00.000Z",
    "firstName": "Ava",
    "lastName": "Chen",
    "street": "string",
    "templateId": 1,
    "zip": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `city` | string | yes | Recipient city. |
| `companyName` | string | no | Recipient company name. |
| `contentVertical` | string | no | Optional vertical text printed on the card edge. |
| `countryCode` | string | yes | Recipient country code. |
| `deliverAt` | date | yes | The mailing date (YYYY-MM-DD). |
| `firstName` | string | yes | Recipient first name. |
| `lastName` | string | yes | Recipient last name. |
| `notificationDate` | date | no | Optional notification date (YYYY-MM-DD). |
| `notificationEmail` | string | no | Optional notification recipient email. |
| `notificationType` | list | no | Optional email timing. One of: `0`, `1`. |
| `sandbox` | list | no | Set to 1 to validate without creating a postcard. One of: `0`, `1`. Default: `1`. |
| `stateCode` | string | no | Recipient state code. |
| `street` | string | yes | Recipient street. |
| `templateId` | number | yes | The template to send. |
| `title` | string | no | Recipient title. |
| `zip` | string | yes | Recipient zip code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EchtPost Postcards API returns.

## Native endpoint

Through the native EchtPost Postcards API, this operation is `POST /cards` (base URL `https://api.echtpost.de/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-card-from-contact-data.md) for the provider-specific parameters and requirements.


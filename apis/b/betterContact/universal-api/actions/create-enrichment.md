# BetterContact: Create Enrichment

Creates an asynchronous BetterContact contact enrichment request.

```
POST https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/create-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BetterContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/create-enrichment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Elon",
  "lastName": "Musk",
  "company": "Tesla",
  "enrichEmailAddress": "true",
  "enrichPhoneNumber": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/create-enrichment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Elon",
    "lastName": "Musk",
    "company": "Tesla",
    "enrichEmailAddress": "true",
    "enrichPhoneNumber": "false"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Contact first name for enrichment. Example: `Elon`. |
| `lastName` | string | yes | Contact last name for enrichment. Example: `Musk`. |
| `company` | string | yes | Company name for enrichment. Example: `Tesla`. |
| `companyDomain` | string | no | Company domain for enrichment. Example: `tesla.com`. |
| `linkedinUrl` | string | no | LinkedIn profile URL for enrichment. Example: `https://www.linkedin.com/in/elonmusk/`. |
| `enrichEmailAddress` | boolean | yes | Whether to enrich work email addresses. Default: `true`. |
| `enrichPhoneNumber` | boolean | yes | Whether to enrich direct phone numbers. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native BetterContact API, this operation is `POST /async` (base URL `https://app.bettercontact.rocks/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-enrichment.md) for the provider-specific parameters and requirements.


# Anyleads: Update Contact

Updates an existing contact in Anyleads.

```
PUT https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anyleads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listName` | string | no | List name for the contact. |
| `subOwner` | string | no | List or campaign owner email. |
| `email` | string | yes | Primary contact email. |
| `score` | number | no | Lead score. |
| `title` | string | no | Contact title. |
| `firstName` | string | no | Contact first name. |
| `middleName` | string | no | Contact middle name. |
| `lastName` | string | no | Contact last name. |
| `jobTitle` | string | no | Contact job title. |
| `phone` | string | no | Contact phone number. |
| `otherEmail` | string | no | Secondary contact email. |
| `linkedinUrl` | string | no | LinkedIn profile URL. |
| `keywords` | string | no | Keywords associated with the contact. |
| `description` | string | no | Contact description. |
| `city` | string | no | Contact city. |
| `region` | string | no | Contact region. |
| `postalCode` | string | no | Contact postal code. |
| `country` | string | no | Contact country. |
| `companyName` | string | no | Related company name. |
| `companyDomain` | string | no | Related company domain. |
| `companyWebsite` | string | no | Related company website. |
| `companyPhone` | string | no | Related company phone. |
| `companyIndustry` | string | no | Related company industry. |
| `companySize` | string | no | Related company size. |
| `companyType` | string | no | Related company type. |
| `companyAddress` | string | no | Related company address. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anyleads API returns.

## Native endpoint

Through the native Anyleads API, this operation is `POST /api-product/incoming-webhook/update-a-contact` (base URL `https://myapiconnect.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.


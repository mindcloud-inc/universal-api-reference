# snapADDY: Create Contact Item



```
POST https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/create-contact-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/create-contact-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attachments[]": [
    "string"
  ],
  "bcChecked": true,
  "bcImage": "string",
  "bcImageBackside": "string",
  "bcImageBacksideLocal": "string",
  "bcImageLocal": "string",
  "city": "string",
  "companySize": "string",
  "contactListId": "string",
  "country": "string",
  "customFields": {},
  "drawing": "string",
  "email": "ava@example.com",
  "facebook": "string",
  "fax": "string",
  "firstName": "Ava",
  "gender": 1,
  "image": "string",
  "industry": "string",
  "lastName": "Chen",
  "linkedin": "https://example.com",
  "mobile": "string",
  "note": "string",
  "organization": "string",
  "phone": "string",
  "poBox": "string",
  "position": "string",
  "revenue": "string",
  "state": "string",
  "street": "string",
  "title": "string",
  "twitter": "string",
  "vat": "string",
  "website": "string",
  "xing": "string",
  "zip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/create-contact-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attachments[]": ["string"],
    "bcChecked": true,
    "bcImage": "string",
    "bcImageBackside": "string",
    "bcImageBacksideLocal": "string",
    "bcImageLocal": "string",
    "city": "string",
    "companySize": "string",
    "contactListId": "string",
    "country": "string",
    "customFields": {},
    "drawing": "string",
    "email": "ava@example.com",
    "facebook": "string",
    "fax": "string",
    "firstName": "Ava",
    "gender": 1,
    "image": "string",
    "industry": "string",
    "lastName": "Chen",
    "linkedin": "https://example.com",
    "mobile": "string",
    "note": "string",
    "organization": "string",
    "phone": "string",
    "poBox": "string",
    "position": "string",
    "revenue": "string",
    "state": "string",
    "street": "string",
    "title": "string",
    "twitter": "string",
    "vat": "string",
    "website": "string",
    "xing": "string",
    "zip": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments[]` | array<string> | yes | Attachment identifiers |
| `bcChecked` | boolean | yes | Whether the business card was checked |
| `bcImage` | string | yes | Business card image URL or content reference |
| `bcImageBackside` | string | yes | Business card backside image URL or content reference |
| `bcImageBacksideLocal` | string | yes | Local backside business card image reference |
| `bcImageLocal` | string | yes | Local business card image reference |
| `city` | string | yes | City |
| `companySize` | string | yes | Company size bucket |
| `contactListId` | string | yes | Contact list identifier |
| `country` | string | yes | Country code |
| `customFields` | object | yes | Custom field map |
| `drawing` | string | yes | Drawing data |
| `email` | string | yes | Email address |
| `facebook` | string | yes | Facebook profile URL |
| `fax` | string | yes | Fax number |
| `firstName` | string | yes | Contact first name |
| `gender` | number | yes | -1 neutral, 0 male, 1 female |
| `image` | string | yes | Profile image |
| `industry` | string | yes | Industry code |
| `lastName` | string | yes | Contact last name |
| `linkedin` | string | yes | LinkedIn profile URL |
| `mobile` | string | yes | Mobile number |
| `note` | string | yes | Contact note |
| `organization` | string | yes | Organization name |
| `phone` | string | yes | Phone number |
| `poBox` | string | yes | PO box |
| `position` | string | yes | Job position |
| `revenue` | string | yes | Revenue |
| `state` | string | yes | State or region |
| `street` | string | yes | Street address |
| `title` | string | yes | Honorific or salutation |
| `twitter` | string | yes | Twitter profile URL |
| `vat` | string | yes | VAT number |
| `website` | string | yes | Website URL |
| `xing` | string | yes | Xing profile URL |
| `zip` | string | yes | ZIP or postal code |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        "string"
      ],
      "city": "string",
      "contactListId": "string",
      "country": "string",
      "created": "string",
      "customFields": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "organization": "string",
      "phone": "string",
      "position": "string",
      "updated": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<string> |  |
| `city` | string |  |
| `contactListId` | string |  |
| `country` | string |  |
| `created` | string |  |
| `customFields` | object |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `organization` | string |  |
| `phone` | string |  |
| `position` | string |  |
| `updated` | string |  |
| `website` | string |  |

## Native endpoint

Through the native snapADDY API, this operation is `POST /grabber/v1/contactitem` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-item.md) for the provider-specific parameters and requirements.


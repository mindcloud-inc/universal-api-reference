# AMcards.com: Get Contact

Retrieves a specific contact from AMcards.com.

```
GET https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AMcards.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-contact?${params}`, {
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
| `contactId` | number | no | AMcards contact identifier from the `/contact/` resource URI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": "string",
      "address": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "country": "string",
        "getCountryDisplay": "string",
        "organization": "string",
        "postalCode": "string",
        "state": "string"
      },
      "addressLine1": "string",
      "addressLine2": "string",
      "anniversaryDay": "string",
      "anniversaryMonth": "string",
      "anniversaryYear": "string",
      "birthDay": "string",
      "birthMonth": "string",
      "birthYear": "string",
      "city": "string",
      "country": "string",
      "emailAddress": "ava@example.com",
      "extraData": "string",
      "firstName": "Ava",
      "groups": "string",
      "id": "string",
      "lastCardSendDate": {},
      "lastName": "Chen",
      "notes": "string",
      "organization": "string",
      "owner": "string",
      "phoneNumber": "string",
      "postalCode": "string",
      "resourceUri": "string",
      "salutation": "string",
      "state": "string",
      "uid": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | string |  |
| `address.addressLine1` | string |  |
| `address.addressLine2` | string |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.getCountryDisplay` | string |  |
| `address.organization` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `addressLine1` | string |  |
| `addressLine2` | string |  |
| `anniversaryDay` | string |  |
| `anniversaryMonth` | string |  |
| `anniversaryYear` | string |  |
| `birthDay` | string |  |
| `birthMonth` | string |  |
| `birthYear` | string |  |
| `city` | string |  |
| `country` | string |  |
| `emailAddress` | string |  |
| `extraData` | string |  |
| `firstName` | string |  |
| `groups` | string |  |
| `id` | string |  |
| `lastCardSendDate` | object |  |
| `lastName` | string |  |
| `notes` | string |  |
| `organization` | string |  |
| `owner` | string |  |
| `phoneNumber` | string |  |
| `postalCode` | string |  |
| `resourceUri` | string |  |
| `salutation` | string |  |
| `state` | string |  |
| `uid` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native AMcards.com API, this operation is `GET /contact/:contactId/` (base URL `https://amcards.com/.api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.


# Simplicate: List Persons



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-persons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-persons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-persons?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "country": "string",
        "countryCode": "string",
        "countryId": "string",
        "id": "string",
        "line1": "string",
        "locality": "string",
        "postalCode": "string",
        "type": "string"
      },
      "avatar": {
        "color": "string",
        "initials": "string"
      },
      "createdAt": "string",
      "dateOfBirth": "string",
      "email": "ava@example.com",
      "facebookUrl": "https://example.com",
      "familyName": "Ava Chen",
      "familyNamePrefix": "Ava Chen",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "gender": "string",
      "genderId": "string",
      "id": "string",
      "initials": "string",
      "isActive": true,
      "linkedinUrl": "https://example.com",
      "mailingListEmail": "ava@example.com",
      "phone": "string",
      "relationType": {
        "color": "string",
        "id": "string",
        "label": "string"
      },
      "simplicateUrl": "https://example.com",
      "timelineEmailAddress": "ava@example.com",
      "twitterUrl": "https://example.com",
      "updatedAt": "string",
      "useCustomSalutation": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.country` | string |  |
| `address.countryCode` | string |  |
| `address.countryId` | string |  |
| `address.id` | string |  |
| `address.line1` | string |  |
| `address.locality` | string |  |
| `address.postalCode` | string |  |
| `address.type` | string |  |
| `avatar.color` | string |  |
| `avatar.initials` | string |  |
| `createdAt` | string |  |
| `dateOfBirth` | string |  |
| `email` | string |  |
| `facebookUrl` | string |  |
| `familyName` | string |  |
| `familyNamePrefix` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `gender` | string |  |
| `genderId` | string |  |
| `id` | string |  |
| `initials` | string |  |
| `isActive` | boolean |  |
| `linkedinUrl` | string |  |
| `mailingListEmail` | string |  |
| `phone` | string |  |
| `relationType.color` | string |  |
| `relationType.id` | string |  |
| `relationType.label` | string |  |
| `simplicateUrl` | string |  |
| `timelineEmailAddress` | string |  |
| `twitterUrl` | string |  |
| `updatedAt` | string |  |
| `useCustomSalutation` | boolean |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /crm/person` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-persons.md) for the provider-specific parameters and requirements.


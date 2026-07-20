# Simplicate: Get Person



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-person?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-person?${params}`, {
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
| `id` | string | yes | The person's id |

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
        "type": "string"
      },
      "avatar": {
        "color": "string",
        "initials": "string"
      },
      "createdAt": "string",
      "email": "ava@example.com",
      "familyName": "Ava Chen",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "gender": "string",
      "genderId": "string",
      "id": "string",
      "isActive": true,
      "mailingListEmail": "ava@example.com",
      "note": "string",
      "relationType": {
        "color": "string",
        "id": "string",
        "label": "string"
      },
      "simplicateUrl": "https://example.com",
      "timelineEmailAddress": "ava@example.com",
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
| `address.type` | string |  |
| `avatar.color` | string |  |
| `avatar.initials` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `familyName` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `gender` | string |  |
| `genderId` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `mailingListEmail` | string |  |
| `note` | string |  |
| `relationType.color` | string |  |
| `relationType.id` | string |  |
| `relationType.label` | string |  |
| `simplicateUrl` | string |  |
| `timelineEmailAddress` | string |  |
| `updatedAt` | string |  |
| `useCustomSalutation` | boolean |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /crm/person/:id` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.


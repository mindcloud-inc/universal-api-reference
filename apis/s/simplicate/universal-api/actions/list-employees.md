# Simplicate: List Employees



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-employees?${params}`, {
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
      "avatar": {
        "color": "string",
        "initials": "string"
      },
      "bankAccount": "string",
      "civilStatus": {
        "id": "string",
        "label": "string"
      },
      "created": "string",
      "createdAt": "string",
      "employmentStatus": "string",
      "hourlyCostTariff": "https://example.com",
      "hourlySalesTariff": "https://example.com",
      "id": "string",
      "isUser": true,
      "modified": "string",
      "name": "Ava Chen",
      "person": {
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
        "dateOfBirth": "string",
        "email": "ava@example.com",
        "facebookUrl": "https://example.com",
        "fullName": "Ava Chen",
        "gender": "string",
        "genderId": "string",
        "id": "string",
        "linkedinUrl": "https://example.com",
        "phone": "string",
        "twitterUrl": "https://example.com"
      },
      "personId": "string",
      "simplicateUrl": "https://example.com",
      "status": {
        "id": "string",
        "label": "string"
      },
      "timelineEmailAddress": "ava@example.com",
      "type": {
        "id": "string",
        "label": "string"
      },
      "updatedAt": "string",
      "workEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar.color` | string |  |
| `avatar.initials` | string |  |
| `bankAccount` | string |  |
| `civilStatus.id` | string |  |
| `civilStatus.label` | string |  |
| `created` | string |  |
| `createdAt` | string |  |
| `employmentStatus` | string |  |
| `hourlyCostTariff` | string |  |
| `hourlySalesTariff` | string |  |
| `id` | string |  |
| `isUser` | boolean |  |
| `modified` | string |  |
| `name` | string |  |
| `person.address.country` | string |  |
| `person.address.countryCode` | string |  |
| `person.address.countryId` | string |  |
| `person.address.id` | string |  |
| `person.address.line1` | string |  |
| `person.address.locality` | string |  |
| `person.address.postalCode` | string |  |
| `person.address.type` | string |  |
| `person.dateOfBirth` | string |  |
| `person.email` | string |  |
| `person.facebookUrl` | string |  |
| `person.fullName` | string |  |
| `person.gender` | string |  |
| `person.genderId` | string |  |
| `person.id` | string |  |
| `person.linkedinUrl` | string |  |
| `person.phone` | string |  |
| `person.twitterUrl` | string |  |
| `personId` | string |  |
| `simplicateUrl` | string |  |
| `status.id` | string |  |
| `status.label` | string |  |
| `timelineEmailAddress` | string |  |
| `type.id` | string |  |
| `type.label` | string |  |
| `updatedAt` | string |  |
| `workEmail` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /hrm/employee` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.


# Simplicate: Get Employee



```
GET https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-employee?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/get-employee?${params}`, {
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
| `id` | string | yes | Employee identifier. |

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
          "type": "string"
        },
        "email": "ava@example.com",
        "fullName": "Ava Chen",
        "gender": "string",
        "genderId": "string",
        "id": "string"
      },
      "personId": "string",
      "simplicateUrl": "https://example.com",
      "status": {
        "id": "string",
        "label": "string"
      },
      "supervisor": {
        "id": "string",
        "name": "Ava Chen",
        "personId": "string"
      },
      "timelineEmailAddress": "ava@example.com",
      "type": {
        "id": "string",
        "label": "string"
      },
      "updatedAt": "string"
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
| `person.address.type` | string |  |
| `person.email` | string |  |
| `person.fullName` | string |  |
| `person.gender` | string |  |
| `person.genderId` | string |  |
| `person.id` | string |  |
| `personId` | string |  |
| `simplicateUrl` | string |  |
| `status.id` | string |  |
| `status.label` | string |  |
| `supervisor.id` | string |  |
| `supervisor.name` | string |  |
| `supervisor.personId` | string |  |
| `timelineEmailAddress` | string |  |
| `type.id` | string |  |
| `type.label` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `GET /hrm/employee/:id` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.


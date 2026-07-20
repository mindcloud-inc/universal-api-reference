# OfficeMaps: Get Person

Retrieves a person from OfficeMaps by ID.

```
GET https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeMaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-person?connectionId=$CONNECTION_ID&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-person?${params}`, {
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
| `personId` | string | yes | The OfficeMaps person UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultDepartmentId": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "isDisabled": true,
      "lastName": "Chen",
      "personId": "string",
      "personTypeId": 1,
      "personTypeName": "Ava Chen",
      "position": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultDepartmentId` | string | Default department UUID. |
| `displayName` | string | Display name. |
| `email` | string | Email address. |
| `firstName` | string | First name. |
| `isDisabled` | boolean | Whether the person is disabled. |
| `lastName` | string | Last name. |
| `personId` | string | Person UUID. |
| `personTypeId` | number | Person type identifier. |
| `personTypeName` | string | Person type name. |
| `position` | string | Job title or position. |
| `userName` | string | User name. |

## Native endpoint

Through the native OfficeMaps API, this operation is `GET /v1/person/:personId` (base URL `https://api.officemaps.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.


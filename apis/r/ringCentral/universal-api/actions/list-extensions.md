# RingCentral: List Extensions

Retrieves extensions from a RingCentral account.

```
GET https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-extensions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RingCentral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-extensions?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-extensions?${params}`, {
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
| `accountId` | string | yes |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedCountry": {
        "id": "string",
        "isoCode": "string",
        "name": "Ava Chen",
        "uri": "string"
      },
      "contact": {
        "email": "ava@example.com",
        "emailAsLoginName": true,
        "firstName": "Ava",
        "lastName": "Chen",
        "pronouncedName": {
          "prompt": {
            "contentType": "Ava Chen",
            "contentUri": "Ava Chen",
            "id": "Ava Chen"
          },
          "text": "Ava Chen",
          "type": "Ava Chen"
        }
      },
      "creationTime": "string",
      "extensionNumber": "string",
      "hidden": true,
      "id": 1,
      "name": "Ava Chen",
      "permissions": {
        "admin": {
          "enabled": true
        },
        "internationalCalling": {
          "enabled": true
        }
      },
      "profileImage": {
        "uri": "string"
      },
      "roles": [
        {
          "id": "string"
        }
      ],
      "status": "string",
      "type": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedCountry.id` | string |  |
| `assignedCountry.isoCode` | string |  |
| `assignedCountry.name` | string |  |
| `assignedCountry.uri` | string |  |
| `contact.email` | string |  |
| `contact.emailAsLoginName` | boolean |  |
| `contact.firstName` | string |  |
| `contact.lastName` | string |  |
| `contact.pronouncedName.prompt.contentType` | string |  |
| `contact.pronouncedName.prompt.contentUri` | string |  |
| `contact.pronouncedName.prompt.id` | string |  |
| `contact.pronouncedName.text` | string |  |
| `contact.pronouncedName.type` | string |  |
| `creationTime` | string |  |
| `extensionNumber` | string |  |
| `hidden` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `permissions.admin.enabled` | boolean |  |
| `permissions.internationalCalling.enabled` | boolean |  |
| `profileImage.uri` | string |  |
| `roles[].id` | string |  |
| `status` | string |  |
| `type` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native RingCentral API, this operation is `GET restapi/v1.0/account/:accountId/extension` (base URL `https://platform.ringcentral.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-extensions.md) for the provider-specific parameters and requirements.


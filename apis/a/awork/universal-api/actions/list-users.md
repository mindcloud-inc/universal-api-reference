# Awork: List Users

Retrieves users from Awork.

```
GET https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-users?${params}`, {
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
| `showArchived` | boolean | no | Whether to include archived users. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "hasImage": true,
      "id": "string",
      "isArchived": true,
      "isDeactivated": true,
      "isExternal": true,
      "language": "string",
      "lastName": "Chen",
      "resourceVersion": 1,
      "shouldMigrateToConnect": true,
      "status": {
        "invitationAccepted": true,
        "isDeactivated": true
      },
      "updatedBy": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "userContactInfos": [
        {
          "createdBy": "string",
          "createdOn": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "isAddress": true,
          "subType": "string",
          "type": "string",
          "updatedBy": "string",
          "updatedOn": "2026-05-07T12:00:00.000Z",
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `createdOn` | date |  |
| `firstName` | string |  |
| `hasImage` | boolean |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `isDeactivated` | boolean |  |
| `isExternal` | boolean |  |
| `language` | string |  |
| `lastName` | string |  |
| `resourceVersion` | number |  |
| `shouldMigrateToConnect` | boolean |  |
| `status.invitationAccepted` | boolean |  |
| `status.isDeactivated` | boolean |  |
| `updatedBy` | string |  |
| `updatedOn` | date |  |
| `userContactInfos[].createdBy` | string |  |
| `userContactInfos[].createdOn` | date |  |
| `userContactInfos[].id` | string |  |
| `userContactInfos[].isAddress` | boolean |  |
| `userContactInfos[].subType` | string |  |
| `userContactInfos[].type` | string |  |
| `userContactInfos[].updatedBy` | string |  |
| `userContactInfos[].updatedOn` | date |  |
| `userContactInfos[].value` | string |  |

## Native endpoint

Through the native Awork API, this operation is `GET /users` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.


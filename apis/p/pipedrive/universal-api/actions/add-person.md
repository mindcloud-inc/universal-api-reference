# Pipedrive: Add Person

Creates a new person in Pipedrive.

```
POST https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Full name of the person. |
| `ownerId` | number | no | Owner user ID for the person. |
| `orgId` | number | no | Organization ID linked to the person. |
| `labelIds` | list<number> | no | Label IDs to assign to the person. |
| `emails` | list<object> | no | Array of email objects for the person. |
| `phones` | list<object> | no | Array of phone objects for the person. |
| `visibleTo` | string | no | Visibility setting for the person record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addTime": "string",
      "customFields": {},
      "firstName": "Ava",
      "id": 1,
      "isDeleted": true,
      "lastName": "Chen",
      "name": "Ava Chen",
      "orgId": 1,
      "ownerId": 1,
      "pictureId": {},
      "updateTime": {},
      "visibleTo": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addTime` | string |  |
| `customFields` | object |  |
| `firstName` | string |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `lastName` | string |  |
| `name` | string |  |
| `orgId` | number |  |
| `ownerId` | number |  |
| `pictureId` | object |  |
| `updateTime` | object |  |
| `visibleTo` | number |  |

## Native endpoint

Through the native Pipedrive API, this operation is `POST v2/persons` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-person.md) for the provider-specific parameters and requirements.


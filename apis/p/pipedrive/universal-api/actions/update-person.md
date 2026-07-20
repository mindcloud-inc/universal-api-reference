# Pipedrive: Update Person

Updates an existing person in Pipedrive.

```
PUT https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique ID of the person to update. |
| `name` | string | no | Updated full name of the person. |
| `ownerId` | number | no | Updated owner user ID. |
| `orgId` | number | no | Updated organization ID. |
| `labelIds` | list<number> | no | Updated label IDs for the person. |
| `emails` | list<object> | no | Updated email array for the person. |
| `phones` | list<object> | no | Updated phone array for the person. |
| `visibleTo` | string | no | Updated visibility setting. |

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
      "updateTime": "string",
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
| `updateTime` | string |  |
| `visibleTo` | number |  |

## Native endpoint

Through the native Pipedrive API, this operation is `PATCH v2/persons/:id` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.


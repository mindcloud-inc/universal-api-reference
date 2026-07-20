# Documo: Create Folder

Creates a new folder in Documo.

```
POST https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-folder', {
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
| `name` | string | yes | String \| Required \| Folder name |
| `sharedWithAccount` | boolean | no | Boolean \| Make the folder accessible by users across the account |
| `parentId` | string | no | Uuid \| Parent folder UUID |
| `userId` | string | no | Uuid \| UUID of the user who owns this folder |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "hierarchyLevel": 1,
      "id": 1,
      "name": "Ava Chen",
      "sharedWithAccount": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `hierarchyLevel` | number |  |
| `id` | number |  |
| `name` | string |  |
| `sharedWithAccount` | boolean |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Documo API, this operation is `POST /folders` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.


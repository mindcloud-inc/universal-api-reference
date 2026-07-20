# GoodDay.work: Create Folder

Creates a new folder in GoodDay.work.

```
POST https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "createdByUserId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "createdByUserId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdByUserId` | string | yes | ID of user on whose behalf folder is created. |
| `name` | string | yes | Folder name. |
| `parentProjectId` | string | no | Parent project ID for subfolder. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": 1,
      "id": "string",
      "momentCreated": "string",
      "name": "Ava Chen",
      "ownerUserId": "string",
      "parentProjectId": "string",
      "systemStatus": 1,
      "systemType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | number | Folder color value. |
| `id` | string | Created folder ID. |
| `momentCreated` | string | Creation timestamp. |
| `name` | string | Folder name. |
| `ownerUserId` | string | Folder owner user ID. |
| `parentProjectId` | string | Parent folder/project ID, if any. |
| `systemStatus` | number | Folder system status. |
| `systemType` | string | Record type, expected to be FOLDER. |

## Native endpoint

Through the native GoodDay.work API, this operation is `POST /projects/new-folder` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.


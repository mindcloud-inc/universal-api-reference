# AITable.ai: Create Datasheet

Creates a new datasheet in AITable.ai.

```
POST https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-datasheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-datasheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-datasheet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional datasheet description. Maximum 500 characters. |
| `spaceId` | string | yes | AITable space ID where the datasheet will be created. |
| `name` | string | yes | Name of the datasheet to create. Maximum 100 characters. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | no | Optional folder node ID. If omitted, AITable creates the datasheet in the working directory. |
| `fields[]` | array<object> | no | Optional array of field definitions to create with the datasheet. AITable allows up to 200 fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "fields": [
        {}
      ],
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Creation timestamp. |
| `fields` | array<object> | Created datasheet fields. |
| `id` | string | Created datasheet ID. |

## Native endpoint

Through the native AITable.ai API, this operation is `POST /fusion/v1/spaces/:spaceId/datasheets` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-datasheet.md) for the provider-specific parameters and requirements.


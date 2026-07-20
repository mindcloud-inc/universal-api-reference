# TxtSync: Create Tag

Creates a new tag in TxtSync.

```
POST https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/create-tag', {
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
| `name` | string | yes | Unique tag name. |
| `contactIds` | list<number> | no | Optional contact IDs to subscribe to the new tag. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatedBy": 1,
      "CreatedByApp": 1,
      "CreatedByAppName": "Ava Chen",
      "CreatedByName": "Ava Chen",
      "CreatedDate": "2026-05-07T12:00:00.000Z",
      "ModifiedBy": 1,
      "ModifiedByApp": 1,
      "ModifiedByAppName": "Ava Chen",
      "ModifiedByName": "Ava Chen",
      "ModifiedDate": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "TagID": 1,
      "Type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedBy` | number |  |
| `CreatedByApp` | number |  |
| `CreatedByAppName` | string |  |
| `CreatedByName` | string |  |
| `CreatedDate` | date |  |
| `ModifiedBy` | number |  |
| `ModifiedByApp` | number |  |
| `ModifiedByAppName` | string |  |
| `ModifiedByName` | string |  |
| `ModifiedDate` | date |  |
| `Name` | string |  |
| `TagID` | number |  |
| `Type` | number |  |

## Native endpoint

Through the native TxtSync API, this operation is `POST /tags` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.


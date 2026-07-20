# TxtSync: Get Tag

Retrieves a specific tag from TxtSync.

```
GET https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-tag?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-tag?${params}`, {
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
| `id` | number | yes | Tag identifier. |

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

Through the native TxtSync API, this operation is `GET /tags/:id` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.


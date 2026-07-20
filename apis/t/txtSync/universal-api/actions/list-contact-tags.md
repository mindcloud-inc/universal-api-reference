# TxtSync: List Contact Tags

Retrieves tags associated with a contact in TxtSync.

```
GET https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/list-contact-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/list-contact-tags?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/list-contact-tags?${params}`, {
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
| `id` | number | yes | Contact identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatedBy": 1,
      "CreatedByName": "Ava Chen",
      "CreatedDate": "2026-05-07T12:00:00.000Z",
      "ModifiedBy": 1,
      "ModifiedByName": "Ava Chen",
      "ModifiedDate": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "Subscribed": true,
      "TagID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedBy` | number |  |
| `CreatedByName` | string |  |
| `CreatedDate` | date |  |
| `ModifiedBy` | number |  |
| `ModifiedByName` | string |  |
| `ModifiedDate` | date |  |
| `Name` | string |  |
| `Subscribed` | boolean |  |
| `TagID` | number |  |

## Native endpoint

Through the native TxtSync API, this operation is `GET /contacts/:id/tags` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-tags.md) for the provider-specific parameters and requirements.


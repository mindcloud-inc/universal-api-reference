# CompanyCam: List Photos

Retrieves a list of photos from CompanyCam.

```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-photos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-photos?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-photos?${params}`, {
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
| `projectIds` | number | no | Include photos from one of these project IDs. Accepts multiple values as an array. Example: `101055442`. |
| `startDate` | date | no | Timestamp to return photos captured on or after this value. |
| `endDate` | date | no | Timestamp to return photos captured on or before this value. |
| `userIds` | list<number> | no | Include photos captured by one of these user IDs. Accepts multiple values as an array. |
| `groupIds` | list<number> | no | Include photos captured by users in one of these group IDs. Accepts multiple values as an array. |
| `tagIds` | list<number> | no | Include photos with one of these tag IDs. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capturedAt": "2026-05-07T12:00:00.000Z",
      "companyId": "string",
      "coordinates": {
        "lat": 1,
        "lon": 1
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "creatorType": "string",
      "description": {},
      "hash": "string",
      "id": "string",
      "internal": true,
      "photoUrl": "https://example.com",
      "processingStatus": "string",
      "projectId": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uris": [
        {
          "type": "string",
          "uri": "string",
          "url": "https://example.com"
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
| `capturedAt` | date |  |
| `companyId` | string |  |
| `coordinates.lat` | number |  |
| `coordinates.lon` | number |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `creatorType` | string |  |
| `description` | object |  |
| `hash` | string |  |
| `id` | string |  |
| `internal` | boolean |  |
| `photoUrl` | string |  |
| `processingStatus` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `uris[].type` | string |  |
| `uris[].uri` | string |  |
| `uris[].url` | string |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET photos` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-photos.md) for the provider-specific parameters and requirements.


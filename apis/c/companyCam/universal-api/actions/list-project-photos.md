# CompanyCam: List Project Photos



```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-project-photos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-project-photos?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-project-photos?${params}`, {
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
| `projectId` | string | yes |  |
| `startDate` | date | no | Timestamp to return only photos captured on or after the provided value. |
| `endDate` | date | no | A timestamp to return photos captured on or before the provided value. |
| `userIDs` | list<number> | no | Filter results to include photos captured by one of these user IDs Accepts multiple values as an array. |
| `groupIDs` | list<number> | no | Filter results to include photos captured by users in one of these group IDs Accepts multiple values as an array. |
| `tagIDs` | list<number> | no | Filter results to include photos with one of these tag IDs Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string",
      "processingStatus": "string",
      "internal": true,
      "description": {},
      "capturedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "projectId": "string",
      "companyId": "string",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "creatorType": "string",
      "photoUrl": "https://example.com",
      "hash": "string",
      "coordinates": {
        "lat": 1,
        "lon": 1
      },
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
| `id` | string |  |
| `status` | string |  |
| `processingStatus` | string |  |
| `internal` | boolean |  |
| `description` | object |  |
| `capturedAt` | date |  |
| `createdAt` | date |  |
| `updatedAt` | date |  |
| `projectId` | string |  |
| `companyId` | string |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `creatorType` | string |  |
| `photoUrl` | string |  |
| `hash` | string |  |
| `coordinates.lat` | number |  |
| `coordinates.lon` | number |  |
| `uris[].type` | string |  |
| `uris[].uri` | string |  |
| `uris[].url` | string |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET projects/:projectId/photos` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-photos.md) for the provider-specific parameters and requirements.


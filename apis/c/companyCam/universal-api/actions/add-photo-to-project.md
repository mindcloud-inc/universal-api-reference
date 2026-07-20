# CompanyCam: Add Photo to Project

Adds a photo to a CompanyCam project.

```
POST https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/add-photo-to-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/add-photo-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "photo.uri": "string",
  "photo.captured_at": "2026-05-07T12:00:00.000Z",
  "project_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/add-photo-to-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "photo.uri": "string",
    "photo.captured_at": "2026-05-07T12:00:00.000Z",
    "project_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `photo.coordinates.lat` | number | no |  |
| `photo.uri` | string | yes |  |
| `photo.captured_at` | date | yes | Timestamp when the photo was captured at. |
| `photo.coordinates.lon` | number | no |  |
| `project_id` | string | yes |  |
| `photo` | object | no |  |
| `photo.description` | string | no | A description of the Photo. |
| `photo.coordinates` | object | no |  |
| `photo.tags` | list<string> | no | Accepts multiple values as an array. |

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
      "hash": {},
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
| `hash` | object |  |
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

Through the native CompanyCam API, this operation is `POST projects/:project_id/photos` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-photo-to-project.md) for the provider-specific parameters and requirements.


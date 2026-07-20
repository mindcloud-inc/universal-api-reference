# CompanyCam: Get Photo



```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-photo?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-photo?${params}`, {
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
| `id` | string | yes | ID of the Photo |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capturedAt": 1,
      "companyId": "string",
      "coordinates": {
        "lat": 1,
        "lon": 1
      },
      "createdAt": 1,
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
      "updatedAt": 1,
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
| `capturedAt` | number |  |
| `companyId` | string |  |
| `coordinates.lat` | number |  |
| `coordinates.lon` | number |  |
| `createdAt` | number |  |
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
| `updatedAt` | number |  |
| `uris[].type` | string |  |
| `uris[].uri` | string |  |
| `uris[].url` | string |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET photos/:id` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-photo.md) for the provider-specific parameters and requirements.


# Synchroteam: Get Job Photos

Retrieves photos for a job from Synchroteam.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-job-photos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-job-photos?connectionId=$CONNECTION_ID&identifierType=string&identifierValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifierType": "string",
  "identifierValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/get-job-photos?${params}`, {
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
| `identifierType` | string | yes | Which identifier to use (for example: num, id, myId). |
| `identifierValue` | string | yes | The identifier value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "fileName": "Ava Chen",
      "imageData": "string",
      "job": {
        "id": "string",
        "myId": "string",
        "num": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `fileName` | string |  |
| `imageData` | string |  |
| `job.id` | string |  |
| `job.myId` | string |  |
| `job.num` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `GET /Api/v2/Jobs/Photos` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-photos.md) for the provider-specific parameters and requirements.


# Hippo Video: Get Viewer Profile by Lead Email

Retrieves viewer profiles in Hippo Video by lead email.

```
GET https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-viewer-profile-by-lead-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hippo Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-viewer-profile-by-lead-email?connectionId=$CONNECTION_ID&userEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-viewer-profile-by-lead-email?${params}`, {
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
| `userEmail` | string | yes | Email address of the lead |

## Response

```json
{
  "success": true,
  "data": [
    {
      "loadMore": true,
      "nextPage": 1,
      "page": 1,
      "status": 1,
      "viewerProfile": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `loadMore` | boolean |  |
| `nextPage` | number |  |
| `page` | number |  |
| `status` | number |  |
| `viewerProfile[]` | array<object> |  |
| `viewerProfile[].browser` | string |  |
| `viewerProfile[].device` | string |  |
| `viewerProfile[].email` | string |  |
| `viewerProfile[].ip` | string |  |
| `viewerProfile[].lastViewedTime` | string |  |
| `viewerProfile[].location` | string |  |
| `viewerProfile[].os` | string |  |
| `viewerProfile[].precentagePlayed` | number |  |
| `viewerProfile[].refererUrl` | string |  |
| `viewerProfile[].videoId` | string |  |
| `viewerProfile[].viewerName` | string |  |
| `viewerProfile[].views` | number |  |

## Native endpoint

Through the native Hippo Video API, this operation is `GET /api/v1/me/video/viewer_profile` (base URL `https://www.hippovideo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-viewer-profile-by-lead-email.md) for the provider-specific parameters and requirements.


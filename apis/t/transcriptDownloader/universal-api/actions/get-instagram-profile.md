# Transcript Downloader: Get Instagram Profile

Retrieves an Instagram profile from Transcript Downloader.

```
GET https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-instagram-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transcript Downloader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-instagram-profile?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transcriptDownloader/latest/actions/get-instagram-profile?${params}`, {
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
| `url` | string | yes | The Instagram profile URL. |
| `includeWebhook` | string | no | A public webhook URL to receive the completed result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "avgEngagement": 1,
      "biography": "string",
      "bioHashtags": [
        "string"
      ],
      "businessAddress": "string",
      "categoryName": "Ava Chen",
      "download": {
        "cost": "string",
        "createdAt": "string",
        "id": "string",
        "mediaId": "string",
        "status": "string",
        "type": "string"
      },
      "downloadId": "string",
      "email": "ava@example.com",
      "externalUrl": "https://example.com",
      "fbid": "string",
      "followers": 1,
      "following": 1,
      "fullName": "Ava Chen",
      "hasChannel": true,
      "highlights": [
        "string"
      ],
      "highlightsCount": 1,
      "instagramId": "string",
      "isBusinessAccount": true,
      "isJoinedRecently": true,
      "isPrivate": true,
      "isProfessionalAccount": true,
      "isVerified": true,
      "lastResponse": {
        "createdAt": "string",
        "downloadId": "string",
        "response": "string",
        "status": "string"
      },
      "listCost": 1,
      "listId": "string",
      "message": "string",
      "postsCount": 1,
      "profileImageLink": "https://example.com",
      "profileName": "Ava Chen",
      "profileUrl": "https://example.com",
      "relatedAccounts": [
        {
          "instagramId": "string",
          "isPrivate": true,
          "isVerified": true,
          "profileName": "Ava Chen",
          "userName": "Ava Chen"
        }
      ],
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `avgEngagement` | number |  |
| `biography` | string |  |
| `bioHashtags` | array<string> |  |
| `businessAddress` | string |  |
| `categoryName` | string |  |
| `download` | object |  |
| `download.cost` | string |  |
| `download.createdAt` | string |  |
| `download.id` | string |  |
| `download.mediaId` | string |  |
| `download.status` | string |  |
| `download.type` | string |  |
| `downloadId` | string |  |
| `email` | string |  |
| `externalUrl` | string |  |
| `fbid` | string |  |
| `followers` | number |  |
| `following` | number |  |
| `fullName` | string |  |
| `hasChannel` | boolean |  |
| `highlights` | array<string> |  |
| `highlightsCount` | number |  |
| `instagramId` | string |  |
| `isBusinessAccount` | boolean |  |
| `isJoinedRecently` | boolean |  |
| `isPrivate` | boolean |  |
| `isProfessionalAccount` | boolean |  |
| `isVerified` | boolean |  |
| `lastResponse` | object |  |
| `lastResponse.createdAt` | string |  |
| `lastResponse.downloadId` | string |  |
| `lastResponse.response` | string |  |
| `lastResponse.status` | string |  |
| `listCost` | number |  |
| `listId` | string |  |
| `message` | string |  |
| `postsCount` | number |  |
| `profileImageLink` | string |  |
| `profileName` | string |  |
| `profileUrl` | string |  |
| `relatedAccounts` | array<object> |  |
| `relatedAccounts[].instagramId` | string |  |
| `relatedAccounts[].isPrivate` | boolean |  |
| `relatedAccounts[].isVerified` | boolean |  |
| `relatedAccounts[].profileName` | string |  |
| `relatedAccounts[].userName` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Transcript Downloader API, this operation is `POST /api/instagram/profile` (base URL `https://dashboard.transcriptdownloader.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-instagram-profile.md) for the provider-specific parameters and requirements.


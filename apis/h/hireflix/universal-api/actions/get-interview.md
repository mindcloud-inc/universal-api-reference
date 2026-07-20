# Hireflix: Get Interview

Retrieves an interview from Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-interview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-interview?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-interview?${params}`, {
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
| `variables.id` | string | yes | The Hireflix interview ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answered": true,
      "completedAt": 1,
      "createdAt": 1,
      "disableNotifications": true,
      "expires": 1,
      "externalId": "string",
      "externalLink": {
        "expires": 1,
        "id": "https://example.com",
        "interviewId": "https://example.com",
        "labels": [
          "https://example.com"
        ],
        "positionId": "https://example.com",
        "url": "https://example.com"
      },
      "hash": "string",
      "id": "string",
      "inviteSource": "string",
      "ipAddresses": [
        "string"
      ],
      "language": "string",
      "retakes": 1,
      "shortlistedAt": 1,
      "status": "string",
      "thumbnail": "string",
      "timeToAnswer": 1,
      "timeToThink": 1,
      "updatedAt": 1,
      "url": {
        "private": "https://example.com",
        "public": "https://example.com",
        "short": "https://example.com"
      },
      "userAgents": [
        "string"
      ],
      "userMetadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answered` | boolean |  |
| `completedAt` | number |  |
| `createdAt` | number |  |
| `disableNotifications` | boolean |  |
| `expires` | number |  |
| `externalId` | string |  |
| `externalLink.expires` | number |  |
| `externalLink.id` | string |  |
| `externalLink.interviewId` | string |  |
| `externalLink.labels` | array<string> |  |
| `externalLink.positionId` | string |  |
| `externalLink.url` | string |  |
| `hash` | string |  |
| `id` | string |  |
| `inviteSource` | string |  |
| `ipAddresses` | array<string> |  |
| `language` | string |  |
| `retakes` | number |  |
| `shortlistedAt` | number |  |
| `status` | string |  |
| `thumbnail` | string |  |
| `timeToAnswer` | number |  |
| `timeToThink` | number |  |
| `updatedAt` | number |  |
| `url.private` | string |  |
| `url.public` | string |  |
| `url.short` | string |  |
| `userAgents` | array<string> |  |
| `userMetadata` | object |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-interview.md) for the provider-specific parameters and requirements.


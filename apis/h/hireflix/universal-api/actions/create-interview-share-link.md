# Hireflix: Create Interview Share Link

Creates a shareable interview link in Hireflix.

```
POST https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/create-interview-share-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/create-interview-share-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/create-interview-share-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.id` | string | yes | The Hireflix interview ID. |
| `variables.durationInDays` | number | no | How many days the share link should remain active. |
| `variables.labels` | string | no | Optional labels to attach to the generated share link. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "status": "string",
      "url": {
        "private": "https://example.com",
        "public": "https://example.com",
        "short": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
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
| `status` | string |  |
| `url.private` | string |  |
| `url.public` | string |  |
| `url.short` | string |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-interview-share-link.md) for the provider-specific parameters and requirements.


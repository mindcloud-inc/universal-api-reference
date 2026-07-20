# Bluesky: Get Profile

Retrieves a Bluesky profile by handle or DID.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-profile?connectionId=$CONNECTION_ID&actor=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actor": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-profile?${params}`, {
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
| `actor` | string | yes | Handle or DID of the profile to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associated": {},
      "avatar": "string",
      "banner": "string",
      "createdAt": "string",
      "description": "string",
      "did": "string",
      "displayName": "Ava Chen",
      "followersCount": 1,
      "followsCount": 1,
      "handle": "string",
      "indexedAt": "string",
      "labels": [
        {}
      ],
      "pinnedPost": {},
      "postsCount": 1,
      "verification": {},
      "viewer": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associated` | object |  |
| `avatar` | string |  |
| `banner` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `did` | string |  |
| `displayName` | string |  |
| `followersCount` | number |  |
| `followsCount` | number |  |
| `handle` | string |  |
| `indexedAt` | string |  |
| `labels` | array<object> |  |
| `pinnedPost` | object |  |
| `postsCount` | number |  |
| `verification` | object |  |
| `viewer` | object |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/app.bsky.actor.getProfile` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.


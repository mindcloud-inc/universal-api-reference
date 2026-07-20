# BASIC: Get project public profile

Retrieves a project public profile from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-project-public-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-project-public-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-project-public-profile?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "auth": {
          "redirect_uris": [
            [
              "string"
            ]
          ]
        },
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "profile": {},
        "slug": "string",
        "website": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.auth.redirect_uris[]` | array<string> |  |
| `data.created_at` | date |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.profile` | object |  |
| `data.slug` | string |  |
| `data.website` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /project/{id}/profile` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-public-profile.md) for the provider-specific parameters and requirements.


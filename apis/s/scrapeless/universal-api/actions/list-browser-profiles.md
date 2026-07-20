# Scrapeless: List Browser Profiles

Retrieves browser profiles from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/list-browser-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/list-browser-profiles?connectionId=$CONNECTION_ID&page=string&pageSize=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page": "string",
  "pageSize": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/list-browser-profiles?${params}`, {
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
| `name` | string | no | profile name or id |
| `page` | string | yes | page number (1-based) |
| `pageSize` | string | yes | number of items per page |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": {
        "count": 1,
        "name": "Ava Chen",
        "profileId": "string",
        "size": 1
      },
      "limit": 1,
      "offset": 1,
      "page": 1,
      "totalDocs": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs` | array<object> | profiles |
| `docs.count` | number | session launching count |
| `docs.name` | string | profile name |
| `docs.profileId` | string | profile id |
| `docs.size` | number | profile size |
| `limit` | number | current page limit |
| `offset` | number | current page offset |
| `page` | number | current page |
| `totalDocs` | number | total profiles |
| `totalPages` | number | total pages |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /browser/profiles` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-browser-profiles.md) for the provider-specific parameters and requirements.


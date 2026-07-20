# LaunchNotes: Get Announcement



```
GET https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-announcement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-announcement?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-announcement?${params}`, {
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
| `id` | string | yes | Announcement identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "authorWithFallback": "string",
      "headline": "string",
      "id": "string",
      "publicPermalink": "https://example.com",
      "publishedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the announcement is archived. |
| `authorWithFallback` | string | Announcement author fallback label. |
| `headline` | string | Announcement headline. |
| `id` | string | Announcement identifier. |
| `publicPermalink` | string | Public permalink. |
| `publishedAt` | date | Announcement publish timestamp. |

## Native endpoint

Through the native LaunchNotes API, this operation is `POST /graphql` (base URL `https://app.launchnotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-announcement.md) for the provider-specific parameters and requirements.


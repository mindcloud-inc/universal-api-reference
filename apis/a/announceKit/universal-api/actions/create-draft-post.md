# AnnounceKit: Create Draft Post

Creates a draft post in AnnounceKit.

```
POST https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/create-draft-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnnounceKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/create-draft-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "66505",
  "title": "string",
  "body": "string",
  "localeId": "en"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/create-draft-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "66505",
    "title": "string",
    "body": "string",
    "localeId": "en"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | AnnounceKit project id that will receive the draft post. Defaults to the project id provided for this build. Default: `66505`. |
| `title` | string | yes | Title for the AnnounceKit post content. |
| `body` | string | yes | HTML body for the AnnounceKit post content. AnnounceKit documents support for basic HTML tags. |
| `localeId` | string | yes | Locale id for the post content. The AnnounceKit example uses en. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created AnnounceKit post id. |

## Native endpoint

Through the native AnnounceKit API, this operation is `POST /gq/v2` (base URL `https://announcekit.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-post.md) for the provider-specific parameters and requirements.


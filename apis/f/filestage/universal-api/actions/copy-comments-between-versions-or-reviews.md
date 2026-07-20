# Filestage: Copy Comments Between Versions or Reviews

Copies comments between Filestage versions or reviews.

```
POST https://connect.mindcloud.co/v1/universal/filestage/latest/actions/copy-comments-between-versions-or-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/copy-comments-between-versions-or-reviews" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reviewId": "string",
  "sourceReviewId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/copy-comments-between-versions-or-reviews', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reviewId": "string",
    "sourceReviewId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reviewId` | string | yes | The unique identifier of the **target** review where the comments will be copied to. |
| `sourceReviewId` | string | yes | The ID of the source review to copy the comments from. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `copyAll` | boolean | no | If `true`, all comments from the source are copied. If `false`, only the comments specified in the `commentIds` array are copied. |
| `commentIds[]` | array<string> | no | An array of specific comment IDs to copy from the source review. This is only used when `copyAll` is `false`. |
| `isBetweenVersions` | boolean | no | Determines the copy mode. If `true`, comments are copied from one version to another. If `false`, comments are copied from one review step to another. Default: `false`. |
| `keepAnnotationsAndMarker` | boolean | no | If `true`, the comment's annotations and markers (positions on the file) are included in the copy. If `false`, only the comment text and metadata are copied. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Filestage API returns.

## Native endpoint

Through the native Filestage API, this operation is `POST /reviews/{reviewId}/comments/copy` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-comments-between-versions-or-reviews.md) for the provider-specific parameters and requirements.


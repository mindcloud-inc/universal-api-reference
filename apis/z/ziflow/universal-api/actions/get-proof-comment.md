# Ziflow: Get Proof Comment

Retrieves a proof comment from Ziflow by ID.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-proof-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-proof-comment?connectionId=$CONNECTION_ID&commentId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commentId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/get-proof-comment?${params}`, {
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
| `commentId` | string | yes | The comment ID. |
| `id` | string | yes | The proof ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {
          "download_path": "string",
          "file_name": "Ava Chen"
        }
      ],
      "comment": "string",
      "comment_resolve": {
        "resolve_date": "string",
        "type": "string",
        "unresolve_date": "string"
      },
      "created_at": "string",
      "deleted": true,
      "id": "string",
      "labels": [
        {
          "id": "string",
          "label": "string"
        }
      ],
      "location": {
        "asset_id": "string",
        "end_time": "string",
        "page": 1,
        "start_time": "string"
      },
      "markers": [
        {
          "color": "string",
          "start_point": {
            "x": 1,
            "y": 1
          },
          "svg_path": "string",
          "type": "string"
        }
      ],
      "parent_comment_id": "string",
      "private": true,
      "proof_id": "string",
      "reactions": [
        {
          "reviewer_email": "ava@example.com",
          "type": "string"
        }
      ],
      "replies": [
        {
          "attachments": [
            {
              "download_path": "string",
              "file_name": "Ava Chen"
            }
          ],
          "comment": "string",
          "created_at": "string",
          "deleted": true,
          "id": "string",
          "markers": [
            "string"
          ],
          "parent_comment_id": "string",
          "private": true,
          "proof_id": "string",
          "replies": [
            "string"
          ],
          "reviewer": {
            "email": "ava@example.com"
          },
          "sequence": 1,
          "source": "string"
        }
      ],
      "reviewer": {
        "email": "ava@example.com",
        "reviewer_id": "string"
      },
      "sequence": 1,
      "source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments[].download_path` | string |  |
| `attachments[].file_name` | string |  |
| `comment` | string |  |
| `comment_resolve.resolve_date` | string |  |
| `comment_resolve.type` | string |  |
| `comment_resolve.unresolve_date` | string |  |
| `created_at` | string |  |
| `deleted` | boolean |  |
| `id` | string |  |
| `labels[].id` | string |  |
| `labels[].label` | string |  |
| `location.asset_id` | string |  |
| `location.end_time` | string |  |
| `location.page` | number |  |
| `location.start_time` | string |  |
| `markers[].color` | string |  |
| `markers[].start_point.x` | number |  |
| `markers[].start_point.y` | number |  |
| `markers[].svg_path` | string |  |
| `markers[].type` | string |  |
| `parent_comment_id` | string |  |
| `private` | boolean |  |
| `proof_id` | string |  |
| `reactions[].reviewer_email` | string |  |
| `reactions[].type` | string |  |
| `replies[].attachments[].download_path` | string |  |
| `replies[].attachments[].file_name` | string |  |
| `replies[].comment` | string |  |
| `replies[].created_at` | string |  |
| `replies[].deleted` | boolean |  |
| `replies[].id` | string |  |
| `replies[].markers[]` | string |  |
| `replies[].parent_comment_id` | string |  |
| `replies[].private` | boolean |  |
| `replies[].proof_id` | string |  |
| `replies[].replies[]` | string |  |
| `replies[].reviewer.email` | string |  |
| `replies[].sequence` | number |  |
| `replies[].source` | string |  |
| `reviewer.email` | string |  |
| `reviewer.reviewer_id` | string |  |
| `sequence` | number |  |
| `source` | string |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /proofs/:id/comments/:commentId` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-proof-comment.md) for the provider-specific parameters and requirements.


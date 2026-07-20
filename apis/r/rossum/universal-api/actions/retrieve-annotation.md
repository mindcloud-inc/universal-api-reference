# Rossum: Retrieve Annotation

Retrieves an annotation from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-annotation?connectionId=$CONNECTION_ID&annotationID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "annotationID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-annotation?${params}`, {
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
| `annotationID` | number | yes | ID of the annotation to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignees": [
        "string"
      ],
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "document": "string",
      "email": "ava@example.com",
      "id": 1,
      "labels": [
        "string"
      ],
      "modified_at": "2026-05-07T12:00:00.000Z",
      "queue": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees` | array<string> | Assigned user URLs. |
| `content` | string | Annotation content URL. |
| `created_at` | date | Annotation creation timestamp. |
| `document` | string | Document URL. |
| `email` | string | Related email URL. |
| `id` | number | Rossum annotation ID. |
| `labels` | array<string> | Attached label URLs. |
| `modified_at` | date | Annotation modification timestamp. |
| `queue` | string | Queue URL. |
| `status` | string | Annotation workflow status. |

## Native endpoint

Through the native Rossum API, this operation is `GET /annotations/:annotationID` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-annotation.md) for the provider-specific parameters and requirements.


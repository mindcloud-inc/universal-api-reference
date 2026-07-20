# Filestage: List File Reviews

Retrieves reviews for a Filestage file.

```
GET https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-file-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-file-reviews?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-file-reviews?${params}`, {
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
| `fileId` | string | yes | File Id |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stepId` | string | no | Step Id to filter results by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "decisions": [
        {}
      ],
      "dueDate": "2026-05-07T12:00:00.000Z",
      "fileId": "string",
      "id": "string",
      "status": {
        "state": "string"
      },
      "stepId": "string",
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `decisions` | array<object> |  |
| `dueDate` | date |  |
| `fileId` | string |  |
| `id` | string |  |
| `status` | object |  |
| `status.state` | string |  |
| `stepId` | string |  |
| `versionId` | string |  |

## Native endpoint

Through the native Filestage API, this operation is `GET /files/{fileId}/reviews` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-reviews.md) for the provider-specific parameters and requirements.


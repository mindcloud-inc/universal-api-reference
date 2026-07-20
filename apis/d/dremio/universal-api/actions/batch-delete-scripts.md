# Dremio: Batch Delete Scripts

Deletes scripts from a Dremio project in batch.

```
DELETE https://connect.mindcloud.co/v1/universal/dremio/latest/actions/batch-delete-scripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/batch-delete-scripts?connectionId=$CONNECTION_ID&ids=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dremio/latest/actions/batch-delete-scripts?${params}`, {
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
| `ids` | list<string> | yes |  |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "notFoundIds": [
        "string"
      ],
      "otherErrorIds": [
        "string"
      ],
      "unauthorizedIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notFoundIds` | array<string> |  |
| `otherErrorIds` | array<string> |  |
| `unauthorizedIds` | array<string> |  |

## Native endpoint

Through the native Dremio API, this operation is `POST /projects/:project_id/scripts:batchDelete` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-delete-scripts.md) for the provider-specific parameters and requirements.


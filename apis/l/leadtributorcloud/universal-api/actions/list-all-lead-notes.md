# leadtributor.cloud: List All Lead Notes

Retrieves notes for all leads in leadtributor.cloud.

```
GET https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-all-lead-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a leadtributor.cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-all-lead-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-all-lead-notes?${params}`, {
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
| `continuation` | string | no | Continuation token for the next page of notes. |
| `maxResults` | number | no | Maximum number of notes to return. Default: `100`. |
| `modifiedSince` | string | no | Filter notes by last modification time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "intern": true,
      "leadId": "string",
      "modifiedAt": "string",
      "noteId": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Note creation timestamp. |
| `intern` | boolean | Whether the note is internal. |
| `leadId` | string | Lead ID that owns the note. |
| `modifiedAt` | string | Note modification timestamp. |
| `noteId` | string | Note ID. |
| `text` | string | Note text. |

## Native endpoint

Through the native leadtributor.cloud API, this operation is `GET /notes` (base URL `https://api.leadtributor.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-lead-notes.md) for the provider-specific parameters and requirements.


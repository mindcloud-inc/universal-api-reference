# leadtributor.cloud: List Lead Notes

Retrieves notes for a lead in leadtributor.cloud.

```
GET https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-lead-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a leadtributor.cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-lead-notes?connectionId=$CONNECTION_ID&leadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-lead-notes?${params}`, {
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
| `leadId` | string | yes | ID of the lead whose notes to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "intern": true,
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
| `modifiedAt` | string | Note modification timestamp. |
| `noteId` | string | Note ID. |
| `text` | string | Note text. |

## Native endpoint

Through the native leadtributor.cloud API, this operation is `GET /leads/:leadId/notes` (base URL `https://api.leadtributor.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lead-notes.md) for the provider-specific parameters and requirements.


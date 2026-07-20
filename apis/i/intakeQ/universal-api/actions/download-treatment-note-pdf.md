# IntakeQ: Download Treatment Note PDF

Retrieves a treatment note PDF from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/download-treatment-note-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/download-treatment-note-pdf?connectionId=$CONNECTION_ID&noteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "noteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/download-treatment-note-pdf?${params}`, {
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
| `noteId` | string | yes | The IntakeQ treatment note ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "data": "string",
      "fileName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `data` | string |  |
| `fileName` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /notes/{noteId}/pdf` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-treatment-note-pdf.md) for the provider-specific parameters and requirements.


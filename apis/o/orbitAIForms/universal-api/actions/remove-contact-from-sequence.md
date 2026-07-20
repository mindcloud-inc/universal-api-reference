# Orbit AI (Forms): Remove Contact from Sequence



```
DELETE https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/remove-contact-from-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orbit AI (Forms) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/remove-contact-from-sequence?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/remove-contact-from-sequence?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "sequence_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_id` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `sequence_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Orbit AI (Forms) API, this operation is `DELETE /api/v1/sequences/:id/enrollments` (base URL `https://orbitforms.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contact-from-sequence.md) for the provider-specific parameters and requirements.


# HubSpot: Batch Read Notes

Retrieves notes from HubSpot in a batch.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-notes?connectionId=$CONNECTION_ID&inputs%5B%5D=%5Bobject%20Object%5D&inputs%5B%5D.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputs[]": "[object Object]",
  "inputs[].id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-notes?${params}`, {
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
| `inputs[]` | array<object> | yes | Note IDs or unique-property values to read. |
| `inputs[].id` | string | yes | The note ID or unique-property value for one requested note. |
| `properties[]` | array<string> | no | Properties to return for each note. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertiesWithHistory[]` | array<string> | no | Properties to return with version history. |
| `idProperty` | string | no | Unique property name to use instead of the record ID. |
| `archived` | boolean | no | Whether to return archived notes only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `id` | string |  |
| `properties` | object |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/notes/batch/read` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-read-notes.md) for the provider-specific parameters and requirements.


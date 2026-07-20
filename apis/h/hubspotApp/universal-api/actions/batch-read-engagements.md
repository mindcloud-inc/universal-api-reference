# HubSpot: Batch Read Engagements

Retrieves engagement records from HubSpot in a batch.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-engagements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-engagements?connectionId=$CONNECTION_ID&engagementType=notes&inputs%5B%5D=%5Bobject%20Object%5D&inputs%5B%5D.id=21628658812" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "engagementType": "notes",
  "inputs[]": "[object Object]",
  "inputs[].id": "21628658812"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-engagements?${params}`, {
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
| `engagementType` | list | yes | The CRM activity object type to batch read, such as notes, tasks, calls, emails, or meetings. One of: `calls`, `communications`, `emails`, `meetings`, `notes`, `postal_mail`, `tasks`. Example: `notes`. |
| `inputs[]` | array<object> | yes | The records to batch read. |
| `inputs[].id` | string | yes | The record ID to batch read. Example: `21628658812`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties[]` | array<string> | no | Properties to include in each returned activity record. |
| `propertiesWithHistory[]` | array<string> | no | Properties to include with history values in each returned activity record. |
| `idProperty` | string | no | The unique property to use instead of the default record ID. Example: `hs_object_id`. |
| `archived` | boolean | no | Whether to read archived records. |

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

Through the native HubSpot API, this operation is `POST crm/v3/objects/:engagementType/batch/read` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-read-engagements.md) for the provider-specific parameters and requirements.


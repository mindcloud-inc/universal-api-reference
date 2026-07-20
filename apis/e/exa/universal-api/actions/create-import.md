# Exa: Create Import

Creates a new import in Exa.

```
POST https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-import
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-import" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "count": 1,
  "entity.type": "string",
  "format": "string",
  "size": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-import', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "count": 1,
    "entity.type": "string",
    "format": "string",
    "size": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `count` | number | yes | Number of records in the import. |
| `csv.identifier` | number | no | CSV column index or identifier column setting. |
| `entity.type` | string | yes | Entity type for imported records. |
| `format` | string | yes | Import format, such as csv. |
| `metadata` | object | no | Optional import metadata object. |
| `size` | number | yes | Size of the import file in bytes. |
| `title` | string | no | Optional import title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "entity": {},
      "failedAt": "2026-05-07T12:00:00.000Z",
      "failedMessage": "string",
      "failedReason": "string",
      "format": "string",
      "id": "string",
      "metadata": {},
      "object": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uploadUrl": "https://example.com",
      "uploadValidUntil": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of records in the import. |
| `createdAt` | date | Creation timestamp. |
| `entity` | object | Imported entity configuration. |
| `failedAt` | date | Import failure timestamp. |
| `failedMessage` | string | Human-readable failure message. |
| `failedReason` | string | Reason the import failed. |
| `format` | string | Import format. |
| `id` | string | Unique import identifier. |
| `metadata` | object | Custom metadata. |
| `object` | string | Returned object type. |
| `status` | string | Import status. |
| `title` | string | Import title. |
| `updatedAt` | date | Last update timestamp. |
| `uploadUrl` | string | Presigned upload URL. |
| `uploadValidUntil` | date | Upload URL expiration timestamp. |

## Native endpoint

Through the native Exa API, this operation is `POST /websets/v0/imports` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-import.md) for the provider-specific parameters and requirements.


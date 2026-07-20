# Harvestr.io: Update Company



```
PUT https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvestr.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier (id or clientId) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The name of the company |
| `externalUid` | string | no | External unique identifier for the company from an external system. Set to null to remove |
| `segments[]` | array<string> | no | Array of segment names the company belongs to |
| `segments[]` | array<string> | no | Array of segment names the company belongs to |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "externalUid": "string",
      "id": "string",
      "importId": "string",
      "name": "Ava Chen",
      "segments": {
        "clientId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string | Client identifier |
| `createdAt` | date | Creation date of the company |
| `externalUid` | string | Only defined when external uid has been setup in Harvestr and when the entity has an external uid in source |
| `id` | string | Unique identifier of the company |
| `importId` | string | Only defined when the company was created from XLSX import, equal to its defined ID |
| `name` | string | Name of the company |
| `segments` | array<object> | Segments associated with this company |
| `segments.clientId` | string | Client identifier |
| `segments.createdAt` | date | Creation date of the segment |
| `segments.id` | string | Unique identifier of the segment |
| `segments.name` | string | Name of the segment |
| `segments.updatedAt` | date | Last update date of the segment |
| `updatedAt` | date | Last update date of the company |

## Native endpoint

Through the native Harvestr.io API, this operation is `PATCH /company/{id}` (base URL `https://rest.harvestr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.


# Exa: Get Import

Retrieves an import from Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-import
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-import?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-import?${params}`, {
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
| `id` | string | yes | Import identifier. |

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
      "updatedAt": "2026-05-07T12:00:00.000Z"
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

## Native endpoint

Through the native Exa API, this operation is `GET /websets/v0/imports/:id` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-import.md) for the provider-specific parameters and requirements.


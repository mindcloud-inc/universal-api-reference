# Quire: Get Tag

Retrieves a tag from Quire.

```
GET https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-tag?connectionId=$CONNECTION_ID&oid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "oid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-tag?${params}`, {
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
| `oid` | string | yes | The Quire tag OID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "name": "Ava Chen",
      "oid": "string",
      "project": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `name` | string |  |
| `oid` | string |  |
| `project` | object |  |

## Native endpoint

Through the native Quire API, this operation is `GET tag/:oid` (base URL `https://quire.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.


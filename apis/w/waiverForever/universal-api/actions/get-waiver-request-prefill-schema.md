# WaiverForever: Get Waiver Request Prefill Schema

Retrieves a waiver request prefill schema from WaiverForever.

```
GET https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-waiver-request-prefill-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-waiver-request-prefill-schema?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-waiver-request-prefill-schema?${params}`, {
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
| `groupId` | string | yes | Waiver request group identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$id": "string",
      "$schema": "string",
      "items": {},
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$id` | string | Schema identifier URL. |
| `$schema` | string | JSON Schema dialect URI. |
| `items` | object | Schema for each prefill record item. |
| `title` | string | Schema title. |
| `type` | string | Top-level JSON type. |

## Native endpoint

Through the native WaiverForever API, this operation is `GET /openapi/v2/waiverRequest/:group_id/prefill/schema` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-waiver-request-prefill-schema.md) for the provider-specific parameters and requirements.


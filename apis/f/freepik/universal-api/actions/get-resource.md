# Freepik: Get Resource

Retrieves detailed resource information from Freepik.

```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-resource?connectionId=$CONNECTION_ID&resourceId=138126245" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "138126245"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-resource?${params}`, {
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
| `resourceId` | number | yes | Freepik resource identifier. Default: `138126245`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "available_formats": {},
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "license": "https://example.com",
      "name": "Ava Chen",
      "premium": true,
      "preview": {},
      "slug": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object | Author details. |
| `available_formats` | object | Available file formats. |
| `created` | date | Resource creation timestamp. |
| `id` | number | Resource ID. |
| `license` | string | License URL. |
| `name` | string | Resource name. |
| `premium` | boolean | Whether the resource is premium. |
| `preview` | object | Preview image details. |
| `slug` | string | Resource slug. |
| `type` | string | Resource media type. |
| `url` | string | Freepik resource URL. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/resources/{{resource-id}}` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource.md) for the provider-specific parameters and requirements.


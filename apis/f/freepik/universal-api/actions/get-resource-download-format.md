# Freepik: Get Resource Download Format

Retrieves a Freepik resource download in a specified format.

```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-resource-download-format
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-resource-download-format?connectionId=$CONNECTION_ID&resourceId=138126245&resourceFormat=eps" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "138126245",
  "resourceFormat": "eps"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-resource-download-format?${params}`, {
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
| `resourceFormat` | string | yes | Download format to request for the resource, such as eps when available. Default: `eps`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string | Format file filename. |
| `url` | string | Temporary format download URL. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/resources/{{resource-id}}/download/{{resource-format}}` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource-download-format.md) for the provider-specific parameters and requirements.


# Freepik: Download Resource

Retrieves a Freepik resource download URL.

```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/download-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/download-resource?connectionId=$CONNECTION_ID&resourceId=138126245" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "138126245"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/download-resource?${params}`, {
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
| `resourceId` | number | yes | Freepik resource identifier to download. Default: `138126245`. |

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
| `filename` | string | Downloaded package filename. |
| `url` | string | Temporary download URL. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/resources/{{resource-id}}/download` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-resource.md) for the provider-specific parameters and requirements.


# E2B: Get Build Upload Link

Retrieves a build upload link from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-build-upload-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-build-upload-link?connectionId=$CONNECTION_ID&hash=string&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hash": "string",
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-build-upload-link?${params}`, {
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
| `hash` | string | yes | Hash of the tar file containing build layer files. |
| `templateId` | string | yes | Identifier of the template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | Upload URL for the tar file containing build layer files. |

## Native endpoint

Through the native E2B API, this operation is `GET /templates/{templateID}/files/{hash}` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-build-upload-link.md) for the provider-specific parameters and requirements.


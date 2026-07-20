# Appwrite: Get country flag

Retrieves a country flag from Appwrite.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/avatars-get-flag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/avatars-get-flag?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/avatars-get-flag?${params}`, {
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
| `code` | file | yes | Country Code. ISO Alpha-2 country code format. |
| `width` | number | no | Image width. Pass an integer between 0 to 2000. Defaults to 100. |
| `height` | number | no | Image height. Pass an integer between 0 to 2000. Defaults to 100. |
| `quality` | number | no | Image quality. Pass an integer between 0 to 100. Defaults to keep existing image quality. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Provider response payload. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /avatars/flags/{code}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/avatars-get-flag.md) for the provider-specific parameters and requirements.


# Wati: Get Media by File Name

Retrieves a media file from Wati by file name.

```
GET https://connect.mindcloud.co/v1/universal/wati/latest/actions/get-media-by-file-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wati/latest/actions/get-media-by-file-name?connectionId=$CONNECTION_ID&fileName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wati/latest/actions/get-media-by-file-name?${params}`, {
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
| `fileName` | string | yes | Media file name returned by Wati messages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Raw file bytes represented as numeric buffer values. |
| `type` | string | Buffer wrapper type returned by the runtime for raw media downloads. |

## Native endpoint

Through the native Wati API, this operation is `GET /api/v1/getMedia` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-by-file-name.md) for the provider-specific parameters and requirements.


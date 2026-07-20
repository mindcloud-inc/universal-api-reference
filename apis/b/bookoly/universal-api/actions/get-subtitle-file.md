# Bookoly: Get Subtitle File

Retrieves a specific subtitle file from Bookoly.

```
GET https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/get-subtitle-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookoly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/get-subtitle-file?connectionId=$CONNECTION_ID&subtitleFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subtitleFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookoly/latest/actions/get-subtitle-file?${params}`, {
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
| `subtitleFile` | string | yes | The subtitle file ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bookoly API returns.

## Native endpoint

Through the native Bookoly API, this operation is `GET /subtitleFiles/{subtitleFile}` (base URL `https://bookoly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subtitle-file.md) for the provider-specific parameters and requirements.


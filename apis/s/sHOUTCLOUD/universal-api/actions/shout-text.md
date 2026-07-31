# SHOUTCLOUD: Shout Text



```
GET https://connect.mindcloud.co/v1/universal/sHOUTCLOUD/latest/actions/shout-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SHOUTCLOUD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sHOUTCLOUD/latest/actions/shout-text?connectionId=$CONNECTION_ID&INPUT=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "INPUT": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sHOUTCLOUD/latest/actions/shout-text?${params}`, {
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
| `INPUT` | string | yes | Text to transform. The original SHOUTCLOUD contract requires this exact uppercase JSON body key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "OUTPUT": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `OUTPUT` | string | Uppercase transformed text returned under the exact original SHOUTCLOUD response key. |

## Native endpoint

Through the native SHOUTCLOUD API, this operation is `POST /V1/SHOUT` (base URL `http://API.SHOUTCLOUD.IO`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/shout-text.md) for the provider-specific parameters and requirements.


# Mallabe: Parse User Agent

Retrieves parsed user agent details from Mallabe.

```
GET https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/parse-user-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mallabe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/parse-user-agent?connectionId=$CONNECTION_ID&userAgent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userAgent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/parse-user-agent?${params}`, {
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
| `userAgent` | string | yes | User agent string to parse. |
| `webhookUrl` | string | no | Webhook URL for asynchronous callbacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browserEngineFamily": "string",
      "browserEngineVersion": "string",
      "browserFamily": "string",
      "browserVersion": "string",
      "deviceBrand": "string",
      "deviceModel": "string",
      "osFamily": "string",
      "osVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browserEngineFamily` | string |  |
| `browserEngineVersion` | string |  |
| `browserFamily` | string |  |
| `browserVersion` | string |  |
| `deviceBrand` | string |  |
| `deviceModel` | string |  |
| `osFamily` | string |  |
| `osVersion` | string |  |

## Native endpoint

Through the native Mallabe API, this operation is `POST /uas/parse` (base URL `https://mallabe.p.rapidapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-user-agent.md) for the provider-specific parameters and requirements.


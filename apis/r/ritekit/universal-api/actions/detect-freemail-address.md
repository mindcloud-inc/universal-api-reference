# Ritekit: Detect Freemail Address

Detects whether an email uses a freemail provider.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/detect-freemail-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/detect-freemail-address?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/detect-freemail-address?${params}`, {
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
| `domain` | string | yes | Domain or email value to check for freemail detection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "freemail": true,
      "message": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `freemail` | boolean |  |
| `message` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v2/person-insights/freemail-detection` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-freemail-address.md) for the provider-specific parameters and requirements.


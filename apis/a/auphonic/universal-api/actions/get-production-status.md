# Auphonic: Get Production Status

Retrieves production status from Auphonic.

```
GET https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-production-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auphonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-production-status?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-production-status?${params}`, {
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
| `uuid` | string | yes | UUID of the production. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "statusString": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |
| `statusString` | string |  |

## Native endpoint

Through the native Auphonic API, this operation is `GET /production/:uuid/status.json` (base URL `https://auphonic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-production-status.md) for the provider-specific parameters and requirements.


# Universal API: Get Connection

Retrieves a connection from Universal API.

```
GET https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/get-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universal API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/get-connection?connectionId=$CONNECTION_ID&universalApi=string&serviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "universalApi": "string",
  "serviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/get-connection?${params}`, {
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
| `universalApi` | string | yes | Unified API key such as hris, mdm, or distributors. |
| `serviceId` | string | yes | Connected service identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "serviceId": "string",
      "status": "string",
      "universalApi": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `serviceId` | string |  |
| `status` | string |  |
| `universalApi` | string |  |

## Native endpoint

Through the native Universal API API, this operation is `GET /api/connections/{universalApi}/{serviceId}` (base URL `https://api.prod.universalapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection.md) for the provider-specific parameters and requirements.


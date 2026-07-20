# BunnyCDN: Get SafeHop Statistics

Retrieves SafeHop traffic statistics from BunnyCDN.

```
GET https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-safe-hop-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-safe-hop-statistics?connectionId=$CONNECTION_ID&pullZoneId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pullZoneId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-safe-hop-statistics?${params}`, {
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
| `pullZoneId` | string | yes | The Bunny pull zone ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorKey": "string",
      "Field": "string",
      "Message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorKey` | string |  |
| `Field` | string |  |
| `Message` | string |  |

## Native endpoint

Through the native BunnyCDN API, this operation is `GET /pullzone/:pullZoneId/safehop/statistics` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-safe-hop-statistics.md) for the provider-specific parameters and requirements.


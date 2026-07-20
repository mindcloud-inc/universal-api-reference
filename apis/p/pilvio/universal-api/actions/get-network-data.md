# Pilvio: Get Network Data



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-network-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-network-data?connectionId=$CONNECTION_ID&networkUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "networkUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-network-data?${params}`, {
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
| `networkUuid` | string | yes | UUID of the private network to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "subnet": "string",
      "subnetIpv6": "string",
      "vlanId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `name` | string |  |
| `subnet` | string |  |
| `subnetIpv6` | string |  |
| `vlanId` | number |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /network/network/{network_uuid}` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-network-data.md) for the provider-specific parameters and requirements.


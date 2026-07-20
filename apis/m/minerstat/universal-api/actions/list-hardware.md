# Minerstat: List Hardware

Retrieves mining hardware from the Minerstat catalog.

```
GET https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-hardware
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minerstat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-hardware?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minerstat/latest/actions/list-hardware?${params}`, {
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
| `type` | string | no | Hardware category like gpu or asic. Example: `gpu`. |
| `brand` | string | no | Manufacturer or marketplace like antminer. Example: `antminer`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "algorithms": {},
      "brand": "string",
      "id": "string",
      "name": "Ava Chen",
      "specs": {},
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `algorithms` | object |  |
| `brand` | string |  |
| `id` | string |  |
| `name` | string |  |
| `specs` | object |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Minerstat API, this operation is `GET /v2/hardware` (base URL `https://api.minerstat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-hardware.md) for the provider-specific parameters and requirements.


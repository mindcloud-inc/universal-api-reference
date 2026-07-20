# BunnyCDN: Add DNS Zone

Creates a new DNS zone in BunnyCDN.

```
POST https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/add-dns-zone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/add-dns-zone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/add-dns-zone', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | Domain name of the DNS zone. |

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
| `ErrorKey` | string | Machine-readable Bunny error key returned when the request fails. |
| `Field` | string | Entity field associated with the Bunny error. |
| `Message` | string | Human-readable Bunny error message. |

## Native endpoint

Through the native BunnyCDN API, this operation is `POST /dnszone` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-dns-zone.md) for the provider-specific parameters and requirements.


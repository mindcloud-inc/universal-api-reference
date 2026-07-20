# Postmaster+: Retrieve IP Feed

Retrieves feed items for an IP in Postmaster+.

```
GET https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-ip-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-ip-feed?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-ip-feed?${params}`, {
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
| `date` | string | no | Filter feed items reported on or after this date in Y-m-d format. |
| `id` | string | yes | The ULID of the IP. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ip": {
        "id": "string",
        "value": "string"
      },
      "mailStream": "string",
      "message": "string",
      "rdns": "string",
      "reportedAt": "string",
      "seedMessage": {
        "subject": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ip.id` | string | Related IP ULID. |
| `ip.value` | string | Related IP value. |
| `mailStream` | string | Mail stream name. |
| `message` | string | Feed message when present. |
| `rdns` | string | Reverse DNS value when present. |
| `reportedAt` | string | Feed event timestamp. |
| `seedMessage.subject` | string | Seed message subject when present. |

## Native endpoint

Through the native Postmaster+ API, this operation is `GET /api/v1/ips/:id/feed` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-ip-feed.md) for the provider-specific parameters and requirements.


# Postmaster+: Retrieve Domain Feed

Retrieves feed items for a domain in Postmaster+.

```
GET https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-domain-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-domain-feed?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-domain-feed?${params}`, {
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
| `id` | string | yes | The ULID of the domain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": {
        "id": "string",
        "value": "string"
      },
      "mailStream": "string",
      "message": "string",
      "reportedAt": "string",
      "seedMessage": {
        "subject": "string"
      },
      "spfDomain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain.id` | string | Related domain ULID. |
| `domain.value` | string | Related domain value. |
| `mailStream` | string | Mail stream name. |
| `message` | string | Feed message when present. |
| `reportedAt` | string | Feed event timestamp. |
| `seedMessage.subject` | string | Seed message subject when present. |
| `spfDomain` | string | SPF domain value when present. |

## Native endpoint

Through the native Postmaster+ API, this operation is `GET /api/v1/domains/:id/feed` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-domain-feed.md) for the provider-specific parameters and requirements.


# SignRequest: List Events



```
GET https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-events?${params}`, {
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
| `document.uuid` | string | no | Example: `ca5a8ec0-4d85-4fd0-9c2a-6b4d3d7987b1`. |
| `document.externalId` | string | no | Example: `contract-1234`. |
| `document.signrequest.who` | list<string> | no | One of: `m`, `mo`, `o`. Example: `o`. |
| `document.signrequest.fromEmail` | string | no | Example: `sender@example.com`. |
| `document.status` | list<string> | no | One of: `ca`, `co`, `de`, `do`, `ec`, `es`, `ne`, `sd`, `se`, `si`, `vi`, `xp`. Example: `se`. |
| `document.user.email` | string | no | Example: `signer@example.com`. |
| `document.user.firstName` | string | no | Example: `Alice`. |
| `document.user.lastName` | string | no | Example: `Smith`. |
| `delivered` | string | no | Example: `true`. |
| `deliveredOn` | date | no | Example: `2026-03-12T15:00:00Z`. |
| `timestamp` | date | no | Example: `2026-03-12T15:00:00Z`. |
| `status` | list<string> | no | One of: `error`, `ok`. Example: `ok`. |
| `eventType` | list<string> | no | One of: `cancelled`, `convert_error`, `converted`, `declined`, `downloaded`, `expired`, `sending_error`, `sent`, `signed`, `signer_downloaded`, `signer_email_bounced`, `signer_forwarded`, `signer_signed`, `signer_viewed`, `signer_viewed_email`, `signrequest_received`, `viewed`. Example: `signed`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackStatusCode": 1,
      "delivered": true,
      "deliveredOn": "2026-05-07T12:00:00.000Z",
      "document": {},
      "eventType": "string",
      "signer": {},
      "status": "string",
      "team": {
        "name": "Ava Chen",
        "subdomain": "string",
        "url": "https://example.com"
      },
      "timestamp": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackStatusCode` | number |  |
| `delivered` | boolean |  |
| `deliveredOn` | date |  |
| `document` | object |  |
| `eventType` | string |  |
| `signer` | object |  |
| `status` | string |  |
| `team` | object |  |
| `team.name` | string |  |
| `team.subdomain` | string |  |
| `team.url` | string |  |
| `timestamp` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native SignRequest API, this operation is `GET /events/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.


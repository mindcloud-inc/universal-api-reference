# SignRequest: List Documents



```
GET https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-documents?${params}`, {
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
| `externalId` | string | no |  |
| `signrequestWho` | string | no |  |
| `signrequestFromEmail` | string | no |  |
| `status` | string | no |  |
| `userEmail` | string | no |  |
| `userFirstName` | string | no |  |
| `userLastName` | string | no |  |
| `created` | string | no |  |
| `modified` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUsed": true,
      "attachments": [
        [
          {}
        ]
      ],
      "autoDeleteAfter": "2026-05-07T12:00:00.000Z",
      "autoDeleteDays": 1,
      "autoExpireAfter": "2026-05-07T12:00:00.000Z",
      "autoExpireDays": 1,
      "eventsCallbackUrl": "https://example.com",
      "externalId": "string",
      "file": "string",
      "fileAsPdf": "string",
      "fileFromSf": {},
      "fileFromUrl": "https://example.com",
      "integrations": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "pdf": "string",
      "prefillTags": [
        [
          {}
        ]
      ],
      "processing": true,
      "sandbox": true,
      "securityHash": "string",
      "shortId": "string",
      "signingLog": {},
      "signrequest": {},
      "status": "string",
      "team": {},
      "template": "string",
      "url": "https://example.com",
      "user": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUsed` | boolean |  |
| `attachments[]` | array<object> |  |
| `autoDeleteAfter` | date |  |
| `autoDeleteDays` | number |  |
| `autoExpireAfter` | date |  |
| `autoExpireDays` | number |  |
| `eventsCallbackUrl` | string |  |
| `externalId` | string |  |
| `file` | string |  |
| `fileAsPdf` | string |  |
| `fileFromSf` | object |  |
| `fileFromUrl` | string |  |
| `integrations[]` | array<object> |  |
| `name` | string |  |
| `pdf` | string |  |
| `prefillTags[]` | array<object> |  |
| `processing` | boolean |  |
| `sandbox` | boolean |  |
| `securityHash` | string |  |
| `shortId` | string |  |
| `signingLog` | object |  |
| `signrequest` | object |  |
| `status` | string |  |
| `team` | object |  |
| `template` | string |  |
| `url` | string |  |
| `user` | object |  |
| `user.displayName` | string |  |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.lastName` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native SignRequest API, this operation is `GET /documents/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.


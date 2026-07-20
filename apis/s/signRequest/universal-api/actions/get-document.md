# SignRequest: Get Document



```
GET https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/get-document?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/get-document?${params}`, {
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
| `uuid` | string | yes |  |

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

Through the native SignRequest API, this operation is `GET /documents/:uuid/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.


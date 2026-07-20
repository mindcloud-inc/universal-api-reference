# SignRequest: Search Documents



```
GET https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/search-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/search-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/search-documents?${params}`, {
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
| `q` | string | no | Normal search query |
| `autocomplete` | string | no | Partial search query |
| `name` | string | no | Document name |
| `subdomain` | string | no | Accepts multiple values in one string, delimited by `\|`. |
| `signerEmails` | string | no | Email needed to sign or approve Accepts multiple values in one string, delimited by `\|`. |
| `status` | list<string> | no | Document status filter One of: `ca`, `co`, `de`, `do`, `ec`, `es`, `ne`, `sd`, `se`, `si`, `vi`, `xp`. Accepts multiple values in one string, delimited by `\|`. |
| `who` | list<string> | no | Signer participation filter One of: `m`, `mo`, `o`. Accepts multiple values in one string, delimited by `\|`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | list<string> | no | Export format One of: `csv`, `json`, `xls`. |
| `signerData` | number | no | Set to 1 to export each signer on a separate row |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autocomplete": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "createdTimestamp": 1,
      "extraDocs": [
        [
          {}
        ]
      ],
      "finishedOn": "2026-05-07T12:00:00.000Z",
      "finishedOnTimestamp": 1,
      "fromEmail": "ava@example.com",
      "name": "Ava Chen",
      "nrExtraDocs": "string",
      "parentDoc": "string",
      "processing": true,
      "signerEmails": [
        [
          "ava@example.com"
        ]
      ],
      "status": "string",
      "statusDisplay": "string",
      "subdomain": "string",
      "uuid": "string",
      "who": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autocomplete` | string |  |
| `created` | date |  |
| `createdTimestamp` | number |  |
| `extraDocs[]` | array<object> |  |
| `finishedOn` | date |  |
| `finishedOnTimestamp` | number |  |
| `fromEmail` | string |  |
| `name` | string |  |
| `nrExtraDocs` | string |  |
| `parentDoc` | string |  |
| `processing` | boolean |  |
| `signerEmails[]` | array<string> |  |
| `status` | string |  |
| `statusDisplay` | string |  |
| `subdomain` | string |  |
| `uuid` | string |  |
| `who` | string |  |

## Native endpoint

Through the native SignRequest API, this operation is `GET /documents-search/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-documents.md) for the provider-specific parameters and requirements.


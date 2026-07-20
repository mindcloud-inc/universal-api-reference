# Atlar: Get bank statement content

Retrieves bank statement content from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-bank-statement-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-bank-statement-content?connectionId=$CONNECTION_ID&cid=string&rid=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cid": "string",
  "rid": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-bank-statement-content?${params}`, {
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
| `cid` | string<string> | yes |  |
| `rid` | string<string> | yes |  |
| `id` | string<string> | yes |  |
| `format` | string<string> | no |  |
| `externalIdAsEndToEndId` | boolean<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Atlar API, this operation is `GET /connectivity/v2beta/connections/{cid}/reports/{rid}/bank-statements/{id}/content` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bank-statement-content.md) for the provider-specific parameters and requirements.


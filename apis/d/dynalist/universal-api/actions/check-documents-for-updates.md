# Dynalist: Check Documents For Updates

Checks Dynalist documents for updates.

```
GET https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/check-documents-for-updates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynalist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/check-documents-for-updates?connectionId=$CONNECTION_ID&file_ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/check-documents-for-updates?${params}`, {
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
| `file_ids[]` | array<string> | yes | IDs of the documents to check for latest version numbers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_code": "string",
      "_msg": "string",
      "versions": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_code` | string |  |
| `_msg` | string |  |
| `versions` | object |  |

## Native endpoint

Through the native Dynalist API, this operation is `POST /doc/check_for_updates` (base URL `https://dynalist.io/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-documents-for-updates.md) for the provider-specific parameters and requirements.


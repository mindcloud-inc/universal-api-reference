# fynk: Get Document Stored File

Retrieves a stored file from fynk.

```
GET https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-document-stored-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fynk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-document-stored-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-document-stored-file?${params}`, {
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
| `document` | string | no | Document UUID. Default: `25c718b2-be8b-44e7-858f-3152e7380022`. |
| `storedFile` | string | no | Stored file UUID. Default: `fa6b4152-241b-416a-8951-1c7cc24f6f0e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native fynk API, this operation is `GET /documents/:document/file-storage/:storedFile` (base URL `https://app.fynk.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-stored-file.md) for the provider-specific parameters and requirements.


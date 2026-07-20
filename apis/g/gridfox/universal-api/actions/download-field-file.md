# Gridfox: Download Field File

Downloads a file from a Gridfox record field.

```
GET https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/download-field-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridfox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/download-field-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/download-field-file?${params}`, {
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
| `fieldName` | string | no | Gridfox file field name from the path parameter. |
| `fileName` | string | no | File name from the path parameter. |
| `referenceFieldValue` | string | no | Record reference field value from the path parameter. |
| `tableName` | string | no | Gridfox table name from the path parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gridfox API returns.

## Native endpoint

Through the native Gridfox API, this operation is `GET /data/:tableName/:referenceFieldValue/:fieldName/:fileName` (base URL `https://api.gridfox.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-field-file.md) for the provider-specific parameters and requirements.


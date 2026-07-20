# Coresignal: List Data Request Files

Retrieves files for a bulk data request from Coresignal.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/list-data-request-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/list-data-request-files?connectionId=$CONNECTION_ID&dataRequestId=51110be1-5d6b-456d-9bb1-538915259c39" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataRequestId": "51110be1-5d6b-456d-9bb1-538915259c39"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/list-data-request-files?${params}`, {
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
| `dataRequestId` | string | yes | Data request identifier returned by a bulk collect action. Example: `51110be1-5d6b-456d-9bb1-538915259c39`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data_request_files": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data_request_files` | array<string> |  |

## Native endpoint

Through the native Coresignal API, this operation is `GET /data_requests/:dataRequestId/files` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-request-files.md) for the provider-specific parameters and requirements.


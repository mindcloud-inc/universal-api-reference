# Geral: Get Collected Data

Retrieves collected data from Geral by ID.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-collected-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-collected-data?connectionId=$CONNECTION_ID&datumId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datumId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-collected-data?${params}`, {
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
| `datumId` | number | yes | The collected data record ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "biolink_block_id": 1,
      "data": {},
      "datetime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "link_id": 1,
      "project_id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `biolink_block_id` | number | Biolink block ID. |
| `data` | object | Collected data payload. |
| `datetime` | date | Creation timestamp. |
| `id` | number | Collected data ID. |
| `link_id` | number | Link ID. |
| `project_id` | number | Project ID. |
| `type` | string | Collected data type. |

## Native endpoint

Through the native Geral API, this operation is `GET /data/:datum_id` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collected-data.md) for the provider-specific parameters and requirements.


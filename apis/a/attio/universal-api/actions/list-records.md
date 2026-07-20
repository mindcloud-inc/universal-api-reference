# Attio: List Records

Retrieves records from Attio.

```
GET https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-records?connectionId=$CONNECTION_ID&object=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "object": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-records?${params}`, {
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
| `object` | string | yes | The Attio object slug or UUID whose records you want to query. |
| `limit` | number | no | Maximum number of records to return. |
| `offset` | number | no | Number of matching records to skip before returning results. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | object | no | Records query filter object for the selected Attio object. |
| `sorts[]` | array<object> | no | Sort definitions array for the records query body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": {},
      "values": {},
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the record was created. |
| `id` | object | Record identifier payload containing workspace, object, and record ids. |
| `values` | object | Dynamic attribute value payload for the record. |
| `webUrl` | string | Attio web URL for the record. |

## Native endpoint

Through the native Attio API, this operation is `POST /v2/objects/:object/records/query` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.


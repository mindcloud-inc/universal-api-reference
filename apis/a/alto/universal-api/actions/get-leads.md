# Alto: Get Leads

Retrieves lead records from your Alto account.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-leads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-leads?${params}`, {
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
| `leadStatus` | string | no | Lead status filter. |
| `modifiedFrom` | date | no | Return leads modified on or after this date. |
| `modifiedTo` | date | no | Return leads modified on or before this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "enquiryDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "leadSource": "string",
      "leadStatus": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `createdDate` | date |  |
| `enquiryDate` | date |  |
| `id` | string |  |
| `leadSource` | string |  |
| `leadStatus` | string |  |
| `modifiedDate` | date |  |

## Native endpoint

Through the native Alto API, this operation is `GET /leads` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-leads.md) for the provider-specific parameters and requirements.


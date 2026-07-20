# eSign Genie: Get Envelope Ids

Retrieves envelope IDs from eSign Genie.

```
GET https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-envelope-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-envelope-ids?connectionId=$CONNECTION_ID&dateFrom=2026-05-07T12%3A00%3A00.000Z&dateTo=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateFrom": "2026-05-07T12:00:00.000Z",
  "dateTo": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-envelope-ids?${params}`, {
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
| `dateFrom` | date | yes | Start date for the envelope search range. |
| `dateTo` | date | yes | End date for the envelope search range. |
| `status` | string | no | Optional Foxit eSign envelope status to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allFolderIds": [
        1
      ],
      "message": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allFolderIds[]` | number |  |
| `message` | string |  |
| `result` | string |  |

## Native endpoint

Through the native eSign Genie API, this operation is `GET /folders/getAllFolderIdsByStatus` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-envelope-ids.md) for the provider-specific parameters and requirements.


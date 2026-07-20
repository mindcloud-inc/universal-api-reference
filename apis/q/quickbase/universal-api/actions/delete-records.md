# Quickbase: Delete Record(s)

Deletes records from a Quickbase table.

```
DELETE https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/delete-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/delete-records?connectionId=$CONNECTION_ID&from=string&where=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "where": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/delete-records?${params}`, {
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
| `from` | string | yes | The Quickbase table identifier. |
| `where` | string | yes | Quickbase where clause that selects the records to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "numberDeleted": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numberDeleted` | number | The number of Quickbase records deleted. |

## Native endpoint

Through the native Quickbase API, this operation is `DELETE v1/records` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records.md) for the provider-specific parameters and requirements.


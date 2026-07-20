# QuickFile: Search Journals



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-journals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-journals?connectionId=$CONNECTION_ID&limit=2&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "limit": "2",
  "offset": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-journals?${params}`, {
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
| `limit` | number | yes | Maximum number of journals to return (up to 50). Default: `2`. |
| `offset` | number | yes | Page offset for journal results. Default: `0`. |
| `dateFrom` | date | no | Lower bound for the journal date range. Default: `2000-01-01`. |
| `dateTo` | date | no | Upper bound for the journal date range. Default: `2030-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "description": "string",
      "journalDate": "2026-05-07T12:00:00.000Z",
      "journalId": 1,
      "reference": "string",
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | Journal currency. |
| `description` | string | Journal description. |
| `journalDate` | date | Journal posting date. |
| `journalId` | number | QuickFile journal identifier. |
| `reference` | string | Journal reference or label. |
| `totalAmount` | number | Journal total amount. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /journal/search` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-journals.md) for the provider-specific parameters and requirements.


# Court Drive: Search Court Cases by Number



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-court-cases-by-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-court-cases-by-number?connectionId=$CONNECTION_ID&caseNo=string&courtCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "caseNo": "string",
  "courtCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-court-cases-by-number?${params}`, {
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
| `caseNo` | string | yes | Case number to search for in the selected court. |
| `courtCode` | string | yes | PACER court code for the search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cases": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cases` | array<object> |  |

## Native endpoint

Through the native Court Drive API, this operation is `POST /courts/pacer/{court_code}/cases/search/by-case-number` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-court-cases-by-number.md) for the provider-specific parameters and requirements.


# Court Drive: Search PACER Case by Number



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-pacer-case-by-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-pacer-case-by-number?connectionId=$CONNECTION_ID&caseNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "caseNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/search-pacer-case-by-number?${params}`, {
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
| `caseNumber` | string | yes | PACER case number to search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cases": [
        {}
      ],
      "pages": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cases` | array<object> |  |
| `pages` | object |  |

## Native endpoint

Through the native Court Drive API, this operation is `GET /cases/pacer/search/case_no/{case_number}` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-pacer-case-by-number.md) for the provider-specific parameters and requirements.


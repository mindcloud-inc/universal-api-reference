# Court Drive: Get Case Summary



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-summary?connectionId=$CONNECTION_ID&caseNumber=string&courtCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "caseNumber": "string",
  "courtCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-summary?${params}`, {
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
| `caseNumber` | string | yes | PACER case number for the case summary. |
| `courtCode` | string | yes | PACER court code for the case summary. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "case": {},
      "case_summary": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `case` | object |  |
| `case_summary` | object |  |
| `links` | object |  |

## Native endpoint

Through the native Court Drive API, this operation is `GET /cases/pacer/{court_code}/{case_number}/case_summary` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-case-summary.md) for the provider-specific parameters and requirements.


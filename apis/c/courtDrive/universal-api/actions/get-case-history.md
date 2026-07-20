# Court Drive: Get Case History



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-history?connectionId=$CONNECTION_ID&caseNumber=string&courtCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "caseNumber": "string",
  "courtCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-history?${params}`, {
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
| `caseNumber` | string | yes | PACER case number for the case history. |
| `courtCode` | string | yes | PACER court code for the case history. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | object |  |
| `links` | object |  |

## Native endpoint

Through the native Court Drive API, this operation is `GET /cases/pacer/{court_code}/{case_number}/history` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-case-history.md) for the provider-specific parameters and requirements.


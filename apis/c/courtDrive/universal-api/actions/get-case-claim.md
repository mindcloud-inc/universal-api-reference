# Court Drive: Get Case Claim



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-claim
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-claim?connectionId=$CONNECTION_ID&caseNumber=string&claimNo=string&courtCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "caseNumber": "string",
  "claimNo": "string",
  "courtCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-case-claim?${params}`, {
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
| `caseNumber` | string | yes | PACER case number for the claim. |
| `claimNo` | string | yes | Claim entry number within the case. |
| `courtCode` | string | yes | PACER court code for the claim. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entry": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entry` | object |  |
| `links` | object |  |

## Native endpoint

Through the native Court Drive API, this operation is `GET /cases/pacer/{court_code}/{case_number}/claims/{claim_no}` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-case-claim.md) for the provider-specific parameters and requirements.


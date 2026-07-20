# DMARC Report: List Postmaster Account Records

Retrieves postmaster account records from DMARC Report.

```
GET https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/list-postmaster-account-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/list-postmaster-account-records?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/list-postmaster-account-records?${params}`, {
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
| `email` | string | yes | Email address of the Postmaster account to retrieve cumulative domain data for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Cumulative Postmaster data keyed by domain for the requested Postmaster email address. |

## Native endpoint

Through the native DMARC Report API, this operation is `GET /postmaster_account_records.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-postmaster-account-records.md) for the provider-specific parameters and requirements.


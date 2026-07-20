# DMARC Report: Delete Domain

Deletes a domain from DMARC Report.

```
DELETE https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/delete-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/delete-domain?connectionId=$CONNECTION_ID&accountId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/delete-domain?${params}`, {
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
| `accountId` | string | yes | DMARC Report account identifier from the endpoint path. |
| `id` | string | yes | Domain identifier from the endpoint path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Deletion status message returned by DMARC Report. |
| `status` | number | Deletion status code returned by DMARC Report. |

## Native endpoint

Through the native DMARC Report API, this operation is `DELETE /accounts/:accountId/domains/:id.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-domain.md) for the provider-specific parameters and requirements.


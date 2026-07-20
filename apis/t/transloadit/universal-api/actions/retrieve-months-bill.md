# Transloadit: Retrieve a month's bill

Retrieves a monthly bill from Transloadit.

```
GET https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-months-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-months-bill?connectionId=$CONNECTION_ID&billDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "billDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-months-bill?${params}`, {
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
| `billDate` | string | yes | The monthly bill to retrieve in YYYY-MM format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "month": "string",
      "ok": "string",
      "plan": {},
      "total": 1,
      "used_gb": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `month` | string | Billing month in YYYY-MM format. |
| `ok` | string | Status code returned by Transloadit for bill retrieval. |
| `plan` | object | Plan metadata associated with the monthly bill. |
| `total` | number | Final billed amount for the month. |
| `used_gb` | number | Bandwidth or storage usage counted for the bill. |

## Native endpoint

Through the native Transloadit API, this operation is `GET /bill/:billDate` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-months-bill.md) for the provider-specific parameters and requirements.


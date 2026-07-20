# SMS Connexion: Get Bulk Number Lookup CSV Export

Retrieves a bulk lookup export from SMS Connexion as CSV.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-bulk-number-lookup-csv-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-bulk-number-lookup-csv-export?connectionId=$CONNECTION_ID&lookupBulkId=2fb73a52-38f8-4b45-ae4d-66de84d5e48e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lookupBulkId": "2fb73a52-38f8-4b45-ae4d-66de84d5e48e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-bulk-number-lookup-csv-export?${params}`, {
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
| `lookupBulkId` | string | yes | Bulk lookup UUID. Example: `2fb73a52-38f8-4b45-ae4d-66de84d5e48e`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMS Connexion API returns.

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /numbers/lookup/lookupBulkId/:lookupBulkId/csv` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-number-lookup-csv-export.md) for the provider-specific parameters and requirements.


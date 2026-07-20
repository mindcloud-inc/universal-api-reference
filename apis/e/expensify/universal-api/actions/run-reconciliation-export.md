# Expensify: Run Reconciliation Export

Retrieves a reconciliation export from Expensify.

```
GET https://connect.mindcloud.co/v1/universal/expensify/latest/actions/run-reconciliation-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/run-reconciliation-export?connectionId=$CONNECTION_ID&domain=string&startDate=string&endDate=string&reconciliationType=Unreported&fileExtension=csv" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "startDate": "string",
  "endDate": "string",
  "reconciliationType": "Unreported",
  "fileExtension": "csv"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expensify/latest/actions/run-reconciliation-export?${params}`, {
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
| `domain` | string | yes | The domain to run reconciliation for. |
| `startDate` | string | yes | The inclusive reconciliation start date in yyyy-mm-dd format. |
| `endDate` | string | yes | The inclusive reconciliation end date in yyyy-mm-dd format. |
| `reconciliationType` | string | yes | Unreported or All. One of: `0`, `1`. Default: `Unreported`. |
| `fileExtension` | string | yes | The reconciliation export format. One of: `0`, `1`, `2`, `3`. Default: `csv`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseCode": 1,
      "responseMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseCode` | number |  |
| `responseMessage` | string |  |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-reconciliation-export.md) for the provider-specific parameters and requirements.


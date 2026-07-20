# Rithum DSCO: Get Invoice

Retrieves an invoice from Rithum DSCO.

```
GET https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-invoice-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum DSCO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-invoice-by-id?connectionId=$CONNECTION_ID&key=string&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/get-invoice-by-id?${params}`, {
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
| `key` | string | yes | Required identifier key used to find the invoice. |
| `value` | string | yes | Required identifier value used to find the invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoiceId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoiceId` | string | Invoice identifier. |
| `status` | string | Invoice status. |

## Native endpoint

Through the native Rithum DSCO API, this operation is `GET invoice` (base URL `https://api.dsco.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-by-id.md) for the provider-specific parameters and requirements.


# ClearoutPhone: Create Bulk Phone Number Validation

Creates a bulk phone number validation job in ClearoutPhone.

```
POST https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/create-bulk-phone-number-validation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClearoutPhone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/create-bulk-phone-number-validation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/create-bulk-phone-number-validation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | CSV or XLSX file to upload for bulk validation |
| `countryCode` | string | no | Default country code for rows without an explicit country code Example: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "listId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `listId` | string |  |

## Native endpoint

Through the native ClearoutPhone API, this operation is `POST /phonenumber/bulk` (base URL `https://api.clearoutphone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-phone-number-validation.md) for the provider-specific parameters and requirements.


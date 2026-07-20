# Viewpoint Spectrum: Upsert Customer Bill-To



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/upsert-customer-bill-to
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/upsert-customer-bill-to" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/upsert-customer-bill-to', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `AltAddr1` | string | no |  |
| `AltAddr2` | string | no |  |
| `AltCity` | string | no |  |
| `AltContact` | string | no | Bill-to Contact |
| `AltCountry` | string | no |  |
| `AltEmail` | string | no |  |
| `AltFax` | string | no |  |
| `AltName` | string | no | Bill-to name Required if creating a new Bill-to code. |
| `AltPhone` | string | no |  |
| `AltState` | string | no |  |
| `AltZip` | string | no |  |
| `Billto_Code` | string | no |  |
| `Customer_Code` | string | no |  |
| `Remark` | string | no |  |
| `Status` | string | no |  |
| `Company_Code` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/CustomerBillto` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-customer-bill-to.md) for the provider-specific parameters and requirements.


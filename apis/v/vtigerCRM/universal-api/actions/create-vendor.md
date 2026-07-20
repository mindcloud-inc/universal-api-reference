# Vtiger CRM: Create Vendor

Creates a new vendor in Vtiger CRM.

```
POST https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vtiger CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "element": {
    "vendorname": "Stage3 Default Vendor"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-vendor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "element": {"vendorname":"Stage3 Default Vendor"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `element` | string | yes | JSON object string for the Vendor fields to create. Default: `{"vendorname":"Stage3 Default Vendor"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Vtiger Vendor id. |
| `label` | string | Vendor label. |
| `url` | string | Vendor URL in Vtiger. |

## Native endpoint

Through the native Vtiger CRM API, this operation is `POST /create?elementType=Vendors` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor.md) for the provider-specific parameters and requirements.


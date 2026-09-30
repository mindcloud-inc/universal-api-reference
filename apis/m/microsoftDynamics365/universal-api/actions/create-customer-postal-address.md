# Microsoft Dynamics 365: Create Customer Postal Address



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-customer-postal-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-customer-postal-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-customer-postal-address', {
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
| `dataAreaId` | string | no |  |
| `addressDescription` | string | no |  |
| `customerLegalEntityId` | string | no |  |
| `customerAccountNumber` | string | no |  |
| `addressStreet` | string | no |  |
| `addressCity` | string | no |  |
| `addressState` | string | no |  |
| `addressZipCode` | string | no |  |
| `addressCountryRegionId` | string | no | Default: `USA`. |
| `addressCountryRegionISOCode` | string | no | Default: `US`. |
| `isPostalAddress` | string | no | Yes/No Default: `Yes`. |
| `isPrimary` | string | no | Yes/No Default: `Yes`. |
| `isRoleBusiness` | string | no | Yes/No Default: `Yes`. |
| `isPrivate` | string | no | Yes/No Default: `No`. |
| `isPrivatePostalAddress` | string | no | Yes/No Default: `No`. |
| `isPrimaryTaxRegistration` | string | no | Yes/No Default: `No`. |
| `isRoleDelivery` | string | no | Yes/No Default: `No`. |
| `addressLocationRoles` | string | no | Default: `Business`. |
| `addressDefaultRoles` | string | no | Default: `Business`. |
| `isRoleHome` | string | no | Default: `No`. |
| `isRoleInvoice` | string | no | Default: `No`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `POST CustomerPostalAddresses` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-postal-address.md) for the provider-specific parameters and requirements.


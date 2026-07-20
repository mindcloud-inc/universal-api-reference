# mfr Field Service Management: Update Company

Updates a company in mfr Field Service Management.

```
PUT https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "bodyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "bodyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `bodyId` | string | yes | Record ID in the request body. |
| `name` | string | no | Updated company name. |
| `externalId` | string | no | Updated external identifier. |
| `note` | string | no | Updated company note. |
| `location` | object | no | Company location object. |
| `isPhysicalPerson` | boolean | no | Whether the company is a physical person. |
| `supportTelephone` | string | no | Support phone number. |
| `supportFax` | string | no | Support fax number. |
| `supportMail` | string | no | Support email address. |
| `isSupplier` | boolean | no | Whether the company is a supplier. |
| `mainContactId` | string | no | Main contact identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native mfr Field Service Management API returns.

## Native endpoint

Through the native mfr Field Service Management API, this operation is `PUT Companies({{id}}L)` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.


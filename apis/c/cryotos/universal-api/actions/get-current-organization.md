# Cryotos: Get Current Organization



```
GET https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-current-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryotos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-current-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-current-organization?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "creationDate": "string",
      "customJson": "string",
      "dateTimeFormat": "string",
      "email": "ava@example.com",
      "feedbackCustomJson": "string",
      "id": 1,
      "isWhatsAppEnabledOrg": true,
      "name": "Ava Chen",
      "reportFieldConfigJson": "string",
      "tempName": "Ava Chen",
      "tenantConfig": "string",
      "updationDate": "string",
      "version": 1,
      "workflowType": "string",
      "zoneCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `creationDate` | string |  |
| `customJson` | string |  |
| `dateTimeFormat` | string |  |
| `email` | string |  |
| `feedbackCustomJson` | string |  |
| `id` | number |  |
| `isWhatsAppEnabledOrg` | boolean |  |
| `name` | string |  |
| `reportFieldConfigJson` | string |  |
| `tempName` | string |  |
| `tenantConfig` | string |  |
| `updationDate` | string |  |
| `version` | number |  |
| `workflowType` | string |  |
| `zoneCode` | string |  |

## Native endpoint

Through the native Cryotos API, this operation is `GET /api/organizations/getCurrentOrganizations` (base URL `https://app.cryotos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-organization.md) for the provider-specific parameters and requirements.


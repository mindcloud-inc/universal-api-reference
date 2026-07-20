# Zoho Projects: Get Portal Details

Retrieves portal details from Zoho Projects.

```
GET https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-portal-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-portal-details?connectionId=$CONNECTION_ID&portalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-portal-details?${params}`, {
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
| `portalId` | string | yes | Zoho Projects portal ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "portalDetails": {
        "businessDetails": {
          "dateFormat": "string",
          "endTime": "string",
          "startTime": "string",
          "timeFormat": "string",
          "weekends": [
            [
              "string"
            ]
          ],
          "weekStartDay": "string",
          "weekStartYear": "string",
          "workingDays": [
            [
              "string"
            ]
          ]
        },
        "id": "string",
        "isCustomdomainEnabled": true,
        "logoUrl": "https://example.com",
        "name": "Ava Chen",
        "orgName": "Ava Chen",
        "owner": {
          "businessHoursId": "string",
          "email": "ava@example.com",
          "firstName": "Ava",
          "fullName": "Ava Chen",
          "id": "string",
          "isClientUser": true,
          "lastName": "Chen",
          "name": "Ava Chen",
          "zpuid": "string"
        },
        "planDetails": {
          "bugtrackerServicePlan": "string",
          "projectsServicePlan": "string"
        },
        "storageType": "string",
        "timezone": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `portalDetails.businessDetails.dateFormat` | string |  |
| `portalDetails.businessDetails.endTime` | string |  |
| `portalDetails.businessDetails.startTime` | string |  |
| `portalDetails.businessDetails.timeFormat` | string |  |
| `portalDetails.businessDetails.weekends[]` | array<string> |  |
| `portalDetails.businessDetails.weekStartDay` | string |  |
| `portalDetails.businessDetails.weekStartYear` | string |  |
| `portalDetails.businessDetails.workingDays[]` | array<string> |  |
| `portalDetails.id` | string |  |
| `portalDetails.isCustomdomainEnabled` | boolean |  |
| `portalDetails.logoUrl` | string |  |
| `portalDetails.name` | string |  |
| `portalDetails.orgName` | string |  |
| `portalDetails.owner.businessHoursId` | string |  |
| `portalDetails.owner.email` | string |  |
| `portalDetails.owner.firstName` | string |  |
| `portalDetails.owner.fullName` | string |  |
| `portalDetails.owner.id` | string |  |
| `portalDetails.owner.isClientUser` | boolean |  |
| `portalDetails.owner.lastName` | string |  |
| `portalDetails.owner.name` | string |  |
| `portalDetails.owner.zpuid` | string |  |
| `portalDetails.planDetails.bugtrackerServicePlan` | string |  |
| `portalDetails.planDetails.projectsServicePlan` | string |  |
| `portalDetails.storageType` | string |  |
| `portalDetails.timezone` | string |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `GET /portal/[:PORTALID]` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-portal-details.md) for the provider-specific parameters and requirements.


# smsmode: Get Channel



```
GET https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-channel?connectionId=$CONNECTION_ID&organisationId=string&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organisationId": "string",
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-channel?${params}`, {
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
| `organisationId` | string | yes | Organisation ID path parameter from the smsmode API route. |
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivePeriod": "string",
      "channelId": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "dailyConsumption": 1,
      "dailyConsumptionLimit": 1,
      "defaultCallbackUrlMo": "https://example.com",
      "defaultCallbackUrlStatus": "https://example.com",
      "defaultFromField": "string",
      "flow": "string",
      "fromFieldList": [
        "string"
      ],
      "href": "string",
      "monthlyConsumption": 1,
      "monthlyConsumptionLimit": 1,
      "name": "Ava Chen",
      "organisationId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivePeriod` | string |  |
| `channelId` | string |  |
| `creationDate` | date |  |
| `dailyConsumption` | number |  |
| `dailyConsumptionLimit` | number |  |
| `defaultCallbackUrlMo` | string |  |
| `defaultCallbackUrlStatus` | string |  |
| `defaultFromField` | string |  |
| `flow` | string |  |
| `fromFieldList[]` | string |  |
| `href` | string |  |
| `monthlyConsumption` | number |  |
| `monthlyConsumptionLimit` | number |  |
| `name` | string |  |
| `organisationId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `GET commons/v1/organisations/:organisationId/channels/:channelId` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.


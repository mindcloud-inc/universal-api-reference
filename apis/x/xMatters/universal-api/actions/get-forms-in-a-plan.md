# xMatters: Get forms in a plan

Retrieves forms in a plan from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-forms-in-a-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-forms-in-a-plan?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-forms-in-a-plan?${params}`, {
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
| `embed` | string | no |  |
| `planId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "apiEnabled": true,
          "description": "string",
          "formId": "string",
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "mobileEnabled": true,
          "name": "Ava Chen",
          "plan": {
            "id": "string"
          },
          "recipients": {
            "count": 1,
            "data": [
              {
                "allowDuplicates": true,
                "externallyOwned": true,
                "id": "string",
                "links": {
                  "self": "https://example.com"
                },
                "observedByAll": true,
                "recipientType": "string",
                "targetName": "Ava Chen",
                "useDefaultDevices": true
              }
            ],
            "links": {
              "self": "https://example.com"
            },
            "total": 1
          },
          "responseOptions": {
            "count": 1,
            "data": [
              {
                "action": "string",
                "allowComments": true,
                "contribution": "string",
                "description": "string",
                "id": "string",
                "joinConference": true,
                "number": 1,
                "prompt": "string",
                "text": "string"
              }
            ],
            "links": {
              "self": "https://example.com"
            },
            "total": 1
          },
          "self": "string",
          "senderOverrides": {
            "callerId": "string",
            "displayName": "Ava Chen"
          },
          "uiEnabled": true
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].apiEnabled` | boolean |  |
| `data[].description` | string |  |
| `data[].formId` | string |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].mobileEnabled` | boolean |  |
| `data[].name` | string |  |
| `data[].plan.id` | string |  |
| `data[].recipients.count` | number |  |
| `data[].recipients.data[].allowDuplicates` | boolean |  |
| `data[].recipients.data[].externallyOwned` | boolean |  |
| `data[].recipients.data[].id` | string |  |
| `data[].recipients.data[].links.self` | string |  |
| `data[].recipients.data[].observedByAll` | boolean |  |
| `data[].recipients.data[].recipientType` | string |  |
| `data[].recipients.data[].targetName` | string |  |
| `data[].recipients.data[].useDefaultDevices` | boolean |  |
| `data[].recipients.links.self` | string |  |
| `data[].recipients.total` | number |  |
| `data[].responseOptions.count` | number |  |
| `data[].responseOptions.data[].action` | string |  |
| `data[].responseOptions.data[].allowComments` | boolean |  |
| `data[].responseOptions.data[].contribution` | string |  |
| `data[].responseOptions.data[].description` | string |  |
| `data[].responseOptions.data[].id` | string |  |
| `data[].responseOptions.data[].joinConference` | boolean |  |
| `data[].responseOptions.data[].number` | number |  |
| `data[].responseOptions.data[].prompt` | string |  |
| `data[].responseOptions.data[].text` | string |  |
| `data[].responseOptions.links.self` | string |  |
| `data[].responseOptions.total` | number |  |
| `data[].self` | string |  |
| `data[].senderOverrides.callerId` | string |  |
| `data[].senderOverrides.displayName` | string |  |
| `data[].uiEnabled` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET plans/{planId}/forms` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-forms-in-a-plan.md) for the provider-specific parameters and requirements.


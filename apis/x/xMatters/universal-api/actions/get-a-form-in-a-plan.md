# xMatters: Get a form in a plan

Retrieves a form in a plan from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-form-in-a-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-form-in-a-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-form-in-a-plan?${params}`, {
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
| `formId` | string | no |  |
| `planId` | string | no |  |

## Response

```json
{
  "success": true,
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
      "uiEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiEnabled` | boolean |  |
| `description` | string |  |
| `formId` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `mobileEnabled` | boolean |  |
| `name` | string |  |
| `plan.id` | string |  |
| `recipients.count` | number |  |
| `recipients.data[].allowDuplicates` | boolean |  |
| `recipients.data[].externallyOwned` | boolean |  |
| `recipients.data[].id` | string |  |
| `recipients.data[].links.self` | string |  |
| `recipients.data[].observedByAll` | boolean |  |
| `recipients.data[].recipientType` | string |  |
| `recipients.data[].targetName` | string |  |
| `recipients.data[].useDefaultDevices` | boolean |  |
| `recipients.links.self` | string |  |
| `recipients.total` | number |  |
| `responseOptions.count` | number |  |
| `responseOptions.data[].action` | string |  |
| `responseOptions.data[].allowComments` | boolean |  |
| `responseOptions.data[].contribution` | string |  |
| `responseOptions.data[].description` | string |  |
| `responseOptions.data[].id` | string |  |
| `responseOptions.data[].joinConference` | boolean |  |
| `responseOptions.data[].number` | number |  |
| `responseOptions.data[].prompt` | string |  |
| `responseOptions.data[].text` | string |  |
| `responseOptions.links.self` | string |  |
| `responseOptions.total` | number |  |
| `uiEnabled` | boolean |  |

## Native endpoint

Through the native xMatters API, this operation is `GET plans/{planId}/forms/{formId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-form-in-a-plan.md) for the provider-specific parameters and requirements.


# Cryotos: Get Template



```
GET https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryotos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-template?${params}`, {
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
| `id` | string | yes | The template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "checkinType": "string",
      "creationDate": "string",
      "description": "string",
      "dummyDescription": "string",
      "id": 1,
      "name": "Ava Chen",
      "reportQuerySchema": "string",
      "slaTimeBreachInHours": 1,
      "templateJson": "string",
      "templateType": "string",
      "updationDate": "string",
      "version": 1,
      "workflowId": 1,
      "workflowName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `checkinType` | string |  |
| `creationDate` | string |  |
| `description` | string |  |
| `dummyDescription` | string |  |
| `id` | number |  |
| `name` | string |  |
| `reportQuerySchema` | string |  |
| `slaTimeBreachInHours` | number |  |
| `templateJson` | string |  |
| `templateType` | string |  |
| `updationDate` | string |  |
| `version` | number |  |
| `workflowId` | number |  |
| `workflowName` | string |  |

## Native endpoint

Through the native Cryotos API, this operation is `GET /api/templates/:id` (base URL `https://app.cryotos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.


# Cryotos: List Public Templates



```
GET https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/list-public-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryotos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/list-public-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/list-public-templates?${params}`, {
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
      "checkinType": "string",
      "creationDate": "string",
      "description": "string",
      "dummyDescription": "string",
      "id": 1,
      "name": "Ava Chen",
      "publicTemplateCategoryId": 1,
      "publicTemplateCategoryName": "Ava Chen",
      "slaTimeBreachInHours": 1,
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
| `publicTemplateCategoryId` | number |  |
| `publicTemplateCategoryName` | string |  |
| `slaTimeBreachInHours` | number |  |
| `templateType` | string |  |
| `updationDate` | string |  |
| `version` | number |  |
| `workflowId` | number |  |
| `workflowName` | string |  |

## Native endpoint

Through the native Cryotos API, this operation is `GET /api/publictemplates` (base URL `https://app.cryotos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-templates.md) for the provider-specific parameters and requirements.


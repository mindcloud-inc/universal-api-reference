# ITM Platform: Get Project Budget



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-budget?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-project-budget?${params}`, {
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
| `projectId` | string | yes | The ITM Platform project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualValues": {},
      "bottomUpBudget": {},
      "globalStandardCost": {},
      "lastPecValues": {},
      "topDownBudget": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualValues` | object |  |
| `bottomUpBudget` | object |  |
| `globalStandardCost` | object |  |
| `lastPecValues` | object |  |
| `topDownBudget` | object |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /project/{ProjectId}/budget` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-budget.md) for the provider-specific parameters and requirements.


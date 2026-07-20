# Qntrl: List Cards

Retrieves a list of cards from Qntrl.

```
GET https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/list-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qntrl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/list-cards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/list-cards?${params}`, {
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
| `layout_id` | string | no | Qntrl layout ID. |
| `org_id` | string | no | Qntrl organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobList": [
        {
          "jobId": "string",
          "stageId": "string",
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobList[].jobId` | string |  |
| `jobList[].stageId` | string |  |
| `jobList[].title` | string |  |

## Native endpoint

Through the native Qntrl API, this operation is `GET /[:org_id]/job` (base URL `https://coreapi.qntrl.com/blueprint/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cards.md) for the provider-specific parameters and requirements.


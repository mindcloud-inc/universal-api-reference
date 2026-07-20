# OnePageCRM: List Pipelines

Retrieves pipelines from OnePageCRM.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-pipelines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-pipelines?${params}`, {
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
      "default": true,
      "id": "string",
      "name": "Ava Chen",
      "stages": [
        {
          "label": "string",
          "stage": 1
        }
      ],
      "type": "string",
      "wonColumnEnabled": true,
      "wonColumnName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `stages[].label` | string |  |
| `stages[].stage` | number |  |
| `type` | string |  |
| `wonColumnEnabled` | boolean |  |
| `wonColumnName` | string |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `GET /pipelines` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipelines.md) for the provider-specific parameters and requirements.


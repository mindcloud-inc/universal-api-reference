# xMatters: Get form response options

Retrieves form response options from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-form-response-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-form-response-options?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-form-response-options?${params}`, {
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
| `formId` | string | no |  |
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].action` | string |  |
| `data[].allowComments` | boolean |  |
| `data[].contribution` | string |  |
| `data[].description` | string |  |
| `data[].id` | string |  |
| `data[].joinConference` | boolean |  |
| `data[].number` | number |  |
| `data[].prompt` | string |  |
| `data[].text` | string |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET plans/{planId}/forms/{formId}/response-options` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-form-response-options.md) for the provider-specific parameters and requirements.


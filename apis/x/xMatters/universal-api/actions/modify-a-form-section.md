# xMatters: Modify a form section

Updates a form section in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-form-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-form-section" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-form-section', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bridgeType` | string | no |  |
| `collapsed` | boolean | no |  |
| `form` | string | no |  |
| `formId` | string | no |  |
| `id` | string | no |  |
| `orderNum` | number | no |  |
| `title` | string | no |  |
| `type` | string | no |  |
| `visible` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bridgeType": "string",
      "collapsed": true,
      "form": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "visibility": "string"
      },
      "id": "string",
      "orderNum": 1,
      "title": "string",
      "type": "string",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bridgeType` | string |  |
| `collapsed` | boolean |  |
| `form.id` | string |  |
| `form.links.self` | string |  |
| `form.visibility` | string |  |
| `id` | string |  |
| `orderNum` | number |  |
| `title` | string |  |
| `type` | string |  |
| `visible` | boolean |  |

## Native endpoint

Through the native xMatters API, this operation is `POST forms/{formId}/sections` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-a-form-section.md) for the provider-specific parameters and requirements.


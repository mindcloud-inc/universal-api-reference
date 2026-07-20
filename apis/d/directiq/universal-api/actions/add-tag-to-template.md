# DirectIQ: Add Tag to Template

Adds a tag to a template in DirectIQ.

```
PUT https://connect.mindcloud.co/v1/universal/directiq/latest/actions/add-tag-to-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/add-tag-to-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directiq/latest/actions/add-tag-to-template', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "tagId": 1,
      "templateId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tagId` | number |  |
| `templateId` | number |  |

## Native endpoint

Through the native DirectIQ API, this operation is `POST /core/template/assigntag/{id}` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tag-to-template.md) for the provider-specific parameters and requirements.


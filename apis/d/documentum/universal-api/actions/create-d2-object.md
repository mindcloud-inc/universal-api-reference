# Documentum: Create D2 Object



```
POST https://connect.mindcloud.co/v1/universal/documentum/latest/actions/create-d2-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/create-d2-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "repositoryName": "d2repo",
  "properties": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentum/latest/actions/create-d2-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "repositoryName": "d2repo",
    "properties": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `repositoryName` | string | yes | Documentum repository name. Example: `d2repo`. |
| `properties` | object | yes | JSON object properties for creation, including r_object_type, object_name, and D2 configuration values as needed. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "links": [
        {
          "href": "https://example.com",
          "rel": "https://example.com"
        }
      ],
      "properties": {
        "objectName": "Ava Chen",
        "objectType": "string"
      },
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created object identifier. |
| `links[].href` | string | Object link URL. |
| `links[].rel` | string | Object link relation. |
| `properties.objectName` | string | Object name. |
| `properties.objectType` | string | Object type. |
| `title` | string | Created object title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `POST /repositories/{repositoryName}/object-creation` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-d2-object.md) for the provider-specific parameters and requirements.


# Contentful: Update locale



```
PUT https://connect.mindcloud.co/v1/universal/contentful/latest/actions/update-locale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contentful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contentful/latest/actions/update-locale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentful/latest/actions/update-locale', {
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
| `environmentId` | string | no |  |
| `localeId` | string | no |  |
| `spaceId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "default": true,
      "fallbackCode": "string",
      "name": "Ava Chen",
      "sys": {
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `default` | boolean |  |
| `fallbackCode` | string |  |
| `name` | string |  |
| `sys.id` | string |  |
| `sys.type` | string |  |

## Native endpoint

Through the native Contentful API, this operation is `PUT /spaces/:spaceId/environments/:environmentId/locales/:localeId` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-locale.md) for the provider-specific parameters and requirements.


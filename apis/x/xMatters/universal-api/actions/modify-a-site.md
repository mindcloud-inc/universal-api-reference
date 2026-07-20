# xMatters: Modify a site

Updates a site in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-site', {
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
| `country` | string | no |  |
| `id` | string | no |  |
| `language` | string | no |  |
| `name` | string | no |  |
| `timezone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "address2": "string",
      "city": "string",
      "country": "string",
      "externallyOwned": true,
      "id": "string",
      "language": "string",
      "latitude": 1,
      "links": {
        "self": "https://example.com"
      },
      "longitude": 1,
      "name": "Ava Chen",
      "postalCode": "string",
      "state": "string",
      "status": "string",
      "targetName": "Ava Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `city` | string |  |
| `country` | string |  |
| `externallyOwned` | boolean |  |
| `id` | string |  |
| `language` | string |  |
| `latitude` | number |  |
| `links.self` | string |  |
| `longitude` | number |  |
| `name` | string |  |
| `postalCode` | string |  |
| `state` | string |  |
| `status` | string |  |
| `targetName` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST sites` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-a-site.md) for the provider-specific parameters and requirements.


# Grist: List Organizations

Finds organizations in Grist.

```
GET https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/list-organizations?${params}`, {
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
      "access": "string",
      "createdAt": "string",
      "domain": "string",
      "host": {},
      "id": 1,
      "name": "Ava Chen",
      "owner": {
        "createdAt": "string",
        "id": 1,
        "name": "Ava Chen",
        "options": {
          "locale": "string"
        },
        "picture": {},
        "ref": "string",
        "type": "string"
      },
      "public": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `createdAt` | string |  |
| `domain` | string |  |
| `host` | object |  |
| `id` | number |  |
| `name` | string |  |
| `owner.createdAt` | string |  |
| `owner.id` | number |  |
| `owner.name` | string |  |
| `owner.options.locale` | string |  |
| `owner.picture` | object |  |
| `owner.ref` | string |  |
| `owner.type` | string |  |
| `public` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Grist API, this operation is `GET /orgs` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.


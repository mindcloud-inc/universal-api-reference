# vionvi CRM: List Sources

Retrieves sources from vionvi CRM.

```
GET https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/list-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vionvi CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/list-sources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/list-sources?${params}`, {
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
      "appId": 1,
      "dtCreate": 1,
      "dtUpdate": 1,
      "groupId": 1,
      "id": 1,
      "isActive": 1,
      "k": "string",
      "name": "Ava Chen",
      "typeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | number |  |
| `dtCreate` | number |  |
| `dtUpdate` | number |  |
| `groupId` | number |  |
| `id` | number |  |
| `isActive` | number |  |
| `k` | string |  |
| `name` | string |  |
| `typeId` | number |  |

## Native endpoint

Through the native vionvi CRM API, this operation is `GET /source` (base URL `https://280-crm-api.vionvi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sources.md) for the provider-specific parameters and requirements.


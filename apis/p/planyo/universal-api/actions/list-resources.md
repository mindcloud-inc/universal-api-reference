# Planyo: List Resources

Retrieves resources from Planyo.

```
GET https://connect.mindcloud.co/v1/universal/planyo/latest/actions/list-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/list-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planyo/latest/actions/list-resources?${params}`, {
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
| `detailLevel` | number | no |  |
| `page` | number | no |  |
| `listPublishedOnly` | boolean | no |  |
| `listReservableOnly` | boolean | no |  |
| `listResourceTypes` | string | no |  |
| `adminId` | number | no |  |
| `geolocationRadius` | number | no |  |
| `resourceFilter` | string | no |  |
| `sort` | string | no |  |
| `siteId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "maxPage": 1,
      "resourceCount": 1,
      "resources": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `maxPage` | number |  |
| `resourceCount` | number |  |
| `resources` | object |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resources.md) for the provider-specific parameters and requirements.


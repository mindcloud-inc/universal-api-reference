# NextBus: List Routes

Retrieves routes for an agency from NextBus.

```
GET https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-routes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextBus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-routes?connectionId=$CONNECTION_ID&agencyTag=glendale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agencyTag": "glendale"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-routes?${params}`, {
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
| `agencyTag` | string | yes | Agency tag from List Agencies. Default: `glendale`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shortTitle": "string",
      "tag": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shortTitle` | string | Optional shortened route title. |
| `tag` | string | Route tag. |
| `title` | string | Route display title. |

## Native endpoint

Through the native NextBus API, this operation is `GET /publicXMLFeed` (base URL `https://retro.umoiq.com/service`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-routes.md) for the provider-specific parameters and requirements.


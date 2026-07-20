# Shippo - Legacy: List All Carrier Parcel Templates

Retrieves carrier parcel templates from Shippo.

```
GET https://connect.mindcloud.co/v1/universal/shippo/latest/actions/list-all-carrier-parcel-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippo - Legacy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippo/latest/actions/list-all-carrier-parcel-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shippo/latest/actions/list-all-carrier-parcel-templates?${params}`, {
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
| `include` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiKey` | string | no | Override the authentication API key here |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shippo - Legacy API returns.

## Native endpoint

Through the native Shippo - Legacy API, this operation is `GET /parcel-templates` (base URL `https://api.goshippo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-carrier-parcel-templates.md) for the provider-specific parameters and requirements.


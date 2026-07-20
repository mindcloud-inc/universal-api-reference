# Statistics Netherlands CBS: Get Table Service Metadata

Retrieves service metadata from a Statistics Netherlands CBS table.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-table-service-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-table-service-metadata?connectionId=$CONNECTION_ID&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-table-service-metadata?${params}`, {
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
| `tableIdentifier` | string | yes | CBS StatLine table identifier, for example 83765NED. Required by the service path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rawResponse": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rawResponse` | string | Raw OData table metadata XML response. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET /ODataApi/odata/{{tableIdentifier}}/$metadata` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table-service-metadata.md) for the provider-specific parameters and requirements.


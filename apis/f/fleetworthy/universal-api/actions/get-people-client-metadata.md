# Fleetworthy: Get People Client Metadata



```
GET https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-people-client-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-people-client-metadata?connectionId=$CONNECTION_ID&clientIdOrDisplayId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientIdOrDisplayId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-people-client-metadata?${params}`, {
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
| `clientIdOrDisplayId` | string | yes | The Fleetworthy client UUID or display identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentTypes": {},
      "jobClasses": [
        {}
      ],
      "locations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentTypes` | object | Client document types, including regulated document types. |
| `jobClasses` | array<object> | Fleetworthy job classes and required-document configuration. |
| `locations` | array<object> | Fleetworthy client locations. |

## Native endpoint

Through the native Fleetworthy API, this operation is `GET /people/client-metadata/{clientIdOrDisplayId}` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-people-client-metadata.md) for the provider-specific parameters and requirements.


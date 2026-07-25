# Viewpoint Vista: Get Service Site by SMServiceSiteID

Represents Info, Serviceable Items, Contacts and Notes tabs data found in Viewpoint® Vista™ SM Service Site program.

```
GET https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-service-site-by-sm-service-site-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-service-site-by-sm-service-site-id?connectionId=$CONNECTION_ID&SMServiceSiteID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "SMServiceSiteID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-service-site-by-sm-service-site-id?${params}`, {
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
| `SMServiceSiteID` | string | yes | The SMCustomerID portion of the key used to identify the object. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `GET v1/direct/subscribers/:subscriber_code/vista/sm/2/data/service_sites/cache/id/:SMServiceSiteID` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-site-by-sm-service-site-id.md) for the provider-specific parameters and requirements.


# HubSpot: Delete Property

Deletes an existing property from HubSpot.

```
DELETE https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/delete-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/delete-property?connectionId=$CONNECTION_ID&objectType=string&propertyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectType": "string",
  "propertyName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/delete-property?${params}`, {
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
| `objectType` | string | yes | The HubSpot object type that owns the property, such as deals, contacts, companies, or tickets. |
| `propertyName` | string | yes | The internal name of the property to archive/delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HubSpot API returns.

## Native endpoint

Through the native HubSpot API, this operation is `DELETE crm/v3/properties/:objectType/:propertyName` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-property.md) for the provider-specific parameters and requirements.


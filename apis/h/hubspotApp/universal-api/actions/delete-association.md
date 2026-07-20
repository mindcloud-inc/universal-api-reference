# HubSpot: Delete Association

Deletes an association between HubSpot records.

```
DELETE https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/delete-association
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/delete-association?connectionId=$CONNECTION_ID&objectType=string&objectId=string&toObjectType=string&toObjectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectType": "string",
  "objectId": "string",
  "toObjectType": "string",
  "toObjectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/delete-association?${params}`, {
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
| `objectType` | string | yes |  |
| `objectId` | string | yes |  |
| `toObjectType` | string | yes |  |
| `toObjectId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HubSpot API returns.

## Native endpoint

Through the native HubSpot API, this operation is `DELETE crm/v4/objects/:objectType/:objectId/associations/:toObjectType/:toObjectId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-association.md) for the provider-specific parameters and requirements.


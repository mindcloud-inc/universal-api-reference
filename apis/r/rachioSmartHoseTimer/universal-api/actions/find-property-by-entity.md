# Rachio Smart Hose Timer: Find Property By Entity

Finds a property in Rachio by entity ID.

```
GET https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/find-property-by-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/find-property-by-entity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/find-property-by-entity?${params}`, {
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
| `resourceId.baseStationId` | string | no | Smart Hose Timer base station UUID. Provide only one entity selector. |
| `resourceId.lightingAreaId` | string | no | Lighting area UUID. Provide only one entity selector. |
| `resourceId.locationId` | string | no | Location entity UUID. Provide only one entity selector. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rachio Smart Hose Timer API returns.

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `GET https://cloud-rest.rach.io/property/findPropertyByEntity` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-property-by-entity.md) for the provider-specific parameters and requirements.


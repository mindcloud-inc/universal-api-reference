# Fleetworthy: List Asset Document Notes



```
GET https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/list-asset-document-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/list-asset-document-notes?connectionId=$CONNECTION_ID&parentId=550e8400-e29b-41d4-a716-446655440000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parentId": "550e8400-e29b-41d4-a716-446655440000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/list-asset-document-notes?${params}`, {
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
| `parentId` | string | yes | The unique identifier of the note's parent entity. Example: `550e8400-e29b-41d4-a716-446655440000`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentType` | list<string> | no | The asset document type. One of: `Accident`, `Asset2290`, `MaintenanceEvent`, `MaintenanceInspection`, `MaintenanceRepair`, `Prerequisite`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fleetworthy API returns.

## Native endpoint

Through the native Fleetworthy API, this operation is `GET /assets/documents/asset-document-notes/from-parent/:parentId` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-asset-document-notes.md) for the provider-specific parameters and requirements.


# Permit.io: Get Resource



```
GET https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Permit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-resource?connectionId=$CONNECTION_ID&projId=string&envId=string&resourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projId": "string",
  "envId": "string",
  "resourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-resource?${params}`, {
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
| `projId` | string | yes | Permit project identifier or key. |
| `envId` | string | yes | Permit environment identifier or key. |
| `resourceId` | string | yes | Permit resource identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionGroups": {},
      "actions": {},
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "environmentId": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "projectId": "string",
      "relations": {},
      "roles": {},
      "typeAttributes": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urn": "string",
      "v1compatName": "Ava Chen",
      "v1compatPath": "string",
      "v1compatType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionGroups` | object |  |
| `actions` | object |  |
| `attributes` | object |  |
| `createdAt` | date |  |
| `description` | string |  |
| `environmentId` | string |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `projectId` | string |  |
| `relations` | object |  |
| `roles` | object |  |
| `typeAttributes` | object |  |
| `updatedAt` | date |  |
| `urn` | string |  |
| `v1compatName` | string |  |
| `v1compatPath` | string |  |
| `v1compatType` | string |  |

## Native endpoint

Through the native Permit.io API, this operation is `GET /v2/schema/:projId/:envId/resources/:resourceId` (base URL `https://api.permit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource.md) for the provider-specific parameters and requirements.


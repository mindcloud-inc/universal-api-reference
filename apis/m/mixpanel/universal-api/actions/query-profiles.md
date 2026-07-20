# Mixpanel: Query Profiles

Retrieves profiles from Mixpanel.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-profiles?${params}`, {
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
| `distinctId` | string | no | Single distinct ID to retrieve. Example: `user-1`. |
| `distinctIds` | string | no | JSON array string of distinct IDs to retrieve. Example: `user-1,user-2`. |
| `dataGroupId` | string | no | Group key ID when querying group profiles. Example: `company`. |
| `where` | string | no | Expression used to filter users or groups. Example: `properties["Plan"] == "Pro"`. |
| `outputProperties` | list<string> | no | List of profile properties to return. Example: `$email,Plan`. |
| `sessionId` | string | no | Session identifier from a previous query for paging. Example: `session_abc123`. |
| `page` | number | no | Page number starting at zero. Example: `0`. |
| `behaviors` | number | no | Behavior selector used for profile exports. Example: `1`. |
| `asOfTimestamp` | number | no | Timestamp used with `behaviors` paging. Example: `1710000000`. |
| `filterByCohort` | string | no | JSON object string like {"id":12345}. Example: `[object Object]`. |
| `includeAllUsers` | boolean | no | Include users without profiles when filtering by cohort. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | no | Required when authenticating with a Mixpanel service account. Example: `12345`. |
| `workspaceId` | number | no | Optional Mixpanel workspace ID. Example: `98765`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "computedAt": "string",
      "page": 1,
      "pageSize": 1,
      "results": [
        [
          {}
        ]
      ],
      "sessionId": "string",
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `computedAt` | string |  |
| `page` | number |  |
| `pageSize` | number |  |
| `results[]` | array<object> |  |
| `results[].distinctId` | string |  |
| `results[].properties` | object |  |
| `results[].properties.codexStage4Union[]` | array<string> |  |
| `results[].properties.lastSeen` | string |  |
| `sessionId` | string |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Mixpanel API, this operation is `POST /query/engage` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-profiles.md) for the provider-specific parameters and requirements.


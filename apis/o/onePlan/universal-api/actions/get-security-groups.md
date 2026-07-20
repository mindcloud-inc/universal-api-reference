# OnePlan: Get Security Groups

Retrieves security groups from OnePlan.

```
GET https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-security-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-security-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-security-groups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "__app__": "string",
      "__entity_kind__": "string",
      "_ts": 1,
      "ConfigId": "string",
      "GroupName": "Ava Chen",
      "id": "string",
      "IsDefault": true,
      "License": "string",
      "PermissionSettings": {},
      "RestoreFromId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__app__` | string |  |
| `__entity_kind__` | string |  |
| `_ts` | number |  |
| `ConfigId` | string |  |
| `GroupName` | string |  |
| `id` | string |  |
| `IsDefault` | boolean |  |
| `License` | string |  |
| `PermissionSettings` | object |  |
| `RestoreFromId` | string |  |

## Native endpoint

Through the native OnePlan API, this operation is `GET /securitygroups` (base URL `https://my.oneplan.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-security-groups.md) for the provider-specific parameters and requirements.


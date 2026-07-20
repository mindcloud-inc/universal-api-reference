# VSCO Workspace: Get My Studio

Retrieves your studio details from VSCO Workspace.

```
GET https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-my-studio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VSCO Workspace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-my-studio?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-my-studio?${params}`, {
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
      "cacheVersion": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "dateFormat": "string",
      "decimalSeparator": "string",
      "defaultBrandId": "string",
      "email": "ava@example.com",
      "externalMappings": [
        {}
      ],
      "hidden": true,
      "id": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "plan": {},
      "readonlyEnabled": true,
      "readonlyEnabledAt": {},
      "temperature": "string",
      "thousandsSeparator": "string",
      "timeFormat": "string",
      "timezoneId": "string",
      "weekStartsOn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cacheVersion` | number |  |
| `created` | date | A server timestamp (always in UTC) |
| `currencyCode` | string |  |
| `dateFormat` | string |  |
| `decimalSeparator` | string |  |
| `defaultBrandId` | string | A ULID entity identifier that is nullable. |
| `email` | string |  |
| `externalMappings` | array<object> |  |
| `hidden` | boolean | Whether or not the object is hidden. |
| `id` | string | A lowercase [ULID](https://github.com/ulid/spec) entity identifier |
| `modified` | date | A server timestamp (always in UTC) |
| `name` | string |  |
| `plan` | object |  |
| `readonlyEnabled` | boolean |  |
| `readonlyEnabledAt` | object |  |
| `temperature` | string |  |
| `thousandsSeparator` | string |  |
| `timeFormat` | string |  |
| `timezoneId` | string | A ULID entity identifier that is nullable. |
| `weekStartsOn` | string |  |

## Native endpoint

Through the native VSCO Workspace API, this operation is `GET /studio/me` (base URL `https://workspace.vsco.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-studio.md) for the provider-specific parameters and requirements.


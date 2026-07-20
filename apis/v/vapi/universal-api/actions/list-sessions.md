# Vapi: List Sessions

Retrieves a list of sessions from Vapi.

```
GET https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-sessions?${params}`, {
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
| `id` | string | no | This is the unique identifier for the session to filter by. |
| `name` | string | no | This is the name of the session to filter by. |
| `assistantId` | string | no | This is the ID of the assistant to filter sessions by. |
| `assistantIdAny` | string | no | Filter by multiple assistant IDs. Provide as comma-separated values. |
| `squadId` | string | no | This is the ID of the squad to filter sessions by. |
| `workflowId` | string | no | This is the ID of the workflow to filter sessions by. |
| `numberE164CheckEnabled` | boolean | no | This is the flag to toggle the E164 check for the `number` field. This is an advanced property which should be used if you know your use case requires it. Use cases: - `false`: To allow non-E164 numbers like `+001234567890`, `1234`, or `abc`. This is useful for dialing out to non-E164 numbers on your SIP trunks. - `true` (default): To allow only E164 numbers like `+14155551234`. This is standard for PSTN calls. If `false`, the `number` is still required to only contain alphanumeric characters (regex: `/^\+?[a-zA-Z0-9]+$/`). @default true (E164 check is enabled) |
| `extension` | string | no | This is the extension that will be dialed after the call is answered. |
| `assistantOverrides` | string | no | These are the overrides for the assistant's settings and template variables specific to this customer. This allows customization of the assistant's behavior for individual customers in batch calls. |
| `number` | string | no | This is the number of the customer. |
| `sipUri` | string | no | This is the SIP URI of the customer. |
| `email` | string | no | This is the email of the customer. |
| `externalId` | string | no | This is the external ID of the customer. |
| `customerNumberAny` | string | no | Filter by any of the specified customer phone numbers (comma-separated). |
| `phoneNumberId` | string | no | This will return sessions with the specified phoneNumberId. |
| `phoneNumberIdAny[]` | array<string> | no | This will return sessions with any of the specified phoneNumberIds. |
| `page` | number | no | This is the page number to return. Defaults to 1. |
| `sortOrder` | string | no | This is the sort order for pagination. Defaults to 'DESC'. |
| `limit` | number | no | This is the maximum number of items to return. Defaults to 100. |
| `createdAtGt` | string | no | This will return items where the createdAt is greater than the specified value. |
| `createdAtLt` | string | no | This will return items where the createdAt is less than the specified value. |
| `createdAtGe` | string | no | This will return items where the createdAt is greater than or equal to the specified value. |
| `createdAtLe` | string | no | This will return items where the createdAt is less than or equal to the specified value. |
| `updatedAtGt` | string | no | This will return items where the updatedAt is greater than the specified value. |
| `updatedAtLt` | string | no | This will return items where the updatedAt is less than the specified value. |
| `updatedAtGe` | string | no | This will return items where the updatedAt is greater than or equal to the specified value. |
| `updatedAtLe` | string | no | This will return items where the updatedAt is less than or equal to the specified value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "results": [
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
| `metadata` | object |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Vapi API, this operation is `GET /session` (base URL `https://api.vapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.


# GoSquared: Get Person

Retrieves a person from GoSquared by ID.

```
GET https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoSquared `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-person?connectionId=$CONNECTION_ID&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-person?${params}`, {
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
| `personId` | string | yes | The unique identifier of the person to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "custom": {},
      "email": "ava@example.com",
      "id": "string",
      "leadSourceType": "string",
      "Links": [
        {}
      ],
      "name": "Ava Chen",
      "smartGroups": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Timestamp when the person record was created. |
| `custom` | object | Custom person properties returned by GoSquared. |
| `email` | string | Primary email for the person. |
| `id` | string | GoSquared person identifier. |
| `leadSourceType` | string | Provider-reported source that created the person. |
| `Links` | array<object> | Provider link metadata returned for related person resources. |
| `name` | string | Display name for the person. |
| `smartGroups` | array<string> | Smart group identifiers currently associated with the person. |

## Native endpoint

Through the native GoSquared API, this operation is `GET people/v1/people/:personID` (base URL `https://api.gosquared.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.


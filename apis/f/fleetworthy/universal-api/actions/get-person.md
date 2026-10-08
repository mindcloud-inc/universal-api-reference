# Fleetworthy: Get Person



```
GET https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-person?connectionId=$CONNECTION_ID&personIdOrDisplayId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personIdOrDisplayId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/get-person?${params}`, {
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
| `personIdOrDisplayId` | string | yes | The Fleetworthy person UUID or display identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientRootLocationId": "string",
      "displayId": "string",
      "generalInfo": {},
      "id": "string",
      "jobClass": {},
      "locationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientRootLocationId` | string | Client root location identifier. |
| `displayId` | string | Fleetworthy display identifier. |
| `generalInfo` | object | Core person identity and contact details. |
| `id` | string | Fleetworthy person identifier. |
| `jobClass` | object | The person's Fleetworthy job classification. |
| `locationId` | string | Assigned Fleetworthy location identifier. |

## Native endpoint

Through the native Fleetworthy API, this operation is `GET /people/{personIdOrDisplayId}` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

